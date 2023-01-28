<template>
    <div class="row mt-5">
        <div class="col-md-4 mx-auto">
            <div class="card ">
                <h3 class="text-center bg-primary rounded">Modulo Calculator</h3>

                <form class="form-horizontal mx-auto" style="margin-top: 25px">
                    <div class="form-group d-flex mb-3">
                        <label for="firstnum" class="col-sm-2 control-label">a =</label>
                        <div class="col-md-8">
                            <input type="number" class="form-control" id="firstnum">
                        </div>
                    </div>
                    <div class="form-group d-flex mb-3">
                        <label for="secondnum" class="col-sm-2 control-label">b =</label>
                        <div class="col-md-8">
                            <input type="number" class="form-control" id="secondnum">
                        </div>
                    </div>
                    <div class="form-group d-flex mb-3">
                        <div class="col-md-8">
                            <div class="btn btn-primary">Calculate</div>
                        </div>
                    </div>
                </form>
            </div>
        </div>
    </div>
</template>

<script setup>

</script>