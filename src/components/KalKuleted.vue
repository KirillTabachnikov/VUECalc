<template>
    <div>
        <div class="main">
            <input type="number" v-model.number="op1">
            <input type="number" v-model.number="op2">
            = {{ result }}
        </div>
        <div class="keyboard">
            <button @click="calculate('+')">+</button>
            <button @click="calculate('-')">-</button>
            <button @click="calculate('/')">/</button>
            <button @click="calculate('*')">*</button>
            <button @click="calculate('^')">^</button>
            <button @click="calculate('%')">%</button>
        </div>
    </div>
</template>
  
<script>
export default {
    name: 'Calculator',
    data() {
        return {
            op1: 0,
            op2: 0,
            result: 0,
        }
    },
    methods: {
        sum() {
            const { op1, op2 } = this;
            this.result = op1 + op2;
        },
        sub() {
            const { op1, op2 } = this;
            this.result = op1 - op2;
        },
        div() {
            const { op1, op2 } = this;
            this.result = op1 / op2;
        },
        mult() {
            const { op1, op2 } = this;
            this.result = op1 * op2;
        },
        pow() {
            const { op1, op2 } = this;
            this.result = Math.pow(op1, op2);
        },
        trunc() {
            const { op1, op2 } = this;
            this.result = Math.trunc(op1 / op2);
        },
        calculate(operation) {
            switch (operation) {
                case '+': this.sum(); break;
                case '-': this.sub(); break;
                case '/': this.div(); break;
                case '*': this.mult(); break;
                case '^': this.pow(); break;
                case '%': this.trunc(); break;
            }
        },
    },
}
</script>
  
