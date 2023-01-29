<template>
    <div class="row mt-5">
        <div class="col-md-4 mx-auto">
            <div class="card ">
                <h3 class="text-center text-white bg-primary rounded-top">Modulo Calculator</h3>

                <div class="form-horizontal mx-auto" style="margin-top: 25px">
                    <div class="form-group d-flex mb-3">
                        <label for="firstnum" class="col-sm-2 control-label">a =</label>
                        <div class="col-md-8">
                            <input type="number" class="form-control" id="firstnum" v-model="fnum">
                        </div>
                    </div>
                    <div class="form-group d-flex mb-3">
                        <label for="secondnum" class="col-sm-2 control-label">b =</label>
                        <div class="col-md-8">
                            <input type="number" class="form-control" id="secondnum" v-model="snum">
                        </div>
                    </div>
                    <div class="mb-3">
                        <div class="col-md-8 mx-auto text-center">
                            <button class="btn btn-primary" @click="calculate()">Calculate</button>
                        </div>
                    </div>
                </div>

                <div class="container text-center mb-3">{{result}}</div>
            </div>
        </div>
    </div>
</template>

<script setup>
import {ref} from 'vue'

const fnum = ref(null)
const snum = ref(null)
var result = ref(0)

// const calculate = () => {
//     result = fnum + snum
//     console.log(result)
// }

function calculate() {
    result = fnum + snum
    console.log(result)
}
</script>