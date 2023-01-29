<template>
    <div class="row mt-5">
        <div class="col-md-4 mx-auto">
            <div class="card ">
                <h4 class="mx-auto text-center text-white rounded p-2" style="background-color: #db781b; width: 99%; margin-top: 3px;">Modulo Calculator</h4>

                <p class="text-center" style="margin-top: 25px">a mod b = ?</p>

                <div class="form-horizontal mx-auto" >
                    <div class="form-group d-flex mb-3">
                        <label for="firstnum" class="col-sm-2 control-label">a =</label>
                        <div class="w-75">
                            <input type="number" class="form-control" id="firstnum" v-model="fnum" placeholder="dividend">
                        </div>
                    </div>
                    <div class="form-group d-flex mb-3">
                        <label for="secondnum" class="col-sm-2 control-label">b =</label>
                        <div class="w-75">
                            <input type="number" class="form-control" id="secondnum" v-model="snum" placeholder="modulus (divisor)">
                        </div>
                    </div>
                    <div class="mb-3">
                        <div class="w-75 mx-auto text-center d-flex justify-content-evenly">
                            <button class="btn btn-primary" @click="calculate()">Calculate</button>
                            <button class="btn btn-danger" @click="clear()">Clear</button>
                        </div>
                    </div>
                </div>

                <div class="container text-center mb-3">
                    <h5 class="bg-success text-white w-25 mx-auto">Result:</h5>
                    <div class="card text-center" style="width: 200px; height: 50px; margin: auto;">
                        <p style="margin: auto;">{{fnum}} mod {{snum}} = {{result}}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import {ref} from 'vue'

const fnum = ref()
const snum = ref()
var result = ref()

const calculate = () => {
    result.value = fnum.value % snum.value

}
const clear = () => {
    result.value = null
    fnum.value = null
    snum.value = null
}

</script>