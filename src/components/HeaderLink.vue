<template>
    <div class="headerLink">
        <router-link class="routerLink" :to="fullLocation">{{displayText}}</router-link>
        <div class="lineContainer">
            <div v-if="isActiveSignal" />
            <div class="line" :style="lineWidth"/>
        </div>
    </div>
</template>

<script>
export default {
    name: "HeaderLink",
    props: ['linkLocation','displayText','selection'],
    computed: {
        fullLocation() {
            return "/" + this.linkLocation;
        },
        lineWidth() {
            return {
                'width': String(this.currentLineWidth) + "px",
            }
        },
        isActiveSignal() {
            let signal = this.selection;
            let verdict = null;

            if (signal == this.linkLocation) {
                verdict = true;
            }
            else {
                verdict = false;
            }

            if (verdict && !this.isActive) {
                this.animateUp();
            }
            if (!verdict && this.isActive) {
                this.animateDown();
            }

            return verdict;
        }
    },
    data() {
        return {
            active: false,
            minWidth: 0,
            maxWidth: 100,
            currentLineWidth: 0, //In px.
            animationDurration: 100, //In milliseconds
            numAnimationSteps: 40,
            isActive: false,
        }
    },
    methods: {
        sleep(ms) {
                return new Promise(resolve => setTimeout(resolve, ms));
        },
        async animateUp() {
            let dt = this.animationDurration / this.numAnimationSteps;
            let dW = (this.maxWidth - this.minWidth) / this.numAnimationSteps

            this.currentLineWidth = 0;

            for (let i = 0; i < this.numAnimationSteps; i++) {
                await this.sleep(dt);
                this.currentLineWidth += dW;
            }
            this.isActive = true;
        },
        async animateDown() {
            let dt = this.animationDurration / this.numAnimationSteps;
            let dW = (this.maxWidth - this.minWidth) / this.numAnimationSteps

            this.currentLineWidth = this.maxWidth;

            for (let i = 0; i < this.numAnimationSteps; i++) {
                await this.sleep(dt);
                this.currentLineWidth -= dW;
            }
            this.isActive = false;
        },
    },
}
</script>

<style>
.headerLink {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.routerLink {
    color: #1e5d15;
}

.routerLink:hover {
    color: red;
}

.lineContainer {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 45px;
    height: 20px;
}

.line {
    border-bottom: 5px solid #1e5d15;
}


</style>
