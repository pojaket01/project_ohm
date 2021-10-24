<template>
<div>

    <div class="d-flex flex-row">
        <div class="p-0 m-0 w-1/4 h-full  ">
            <v-sheet class="p-1 m-1 w-3/4 h-full" color="white" elevation="10" height="76vh" width="23vw">
                <div class="p-0 m-0 w-3/4 h-full border-5 line rounded " style="height:75vh; width:22.5vw; ">
                    <pre>{{name}}</pre>
                </div>
            </v-sheet>

        </div>

        <v-sheet class="p-1 m-1 w-3/4 h-full" color="white" elevation="10" height="76vh" width="74.5vw">
            <div class=" p-0 m-0 w-3/4 h-full  border-3 line rounded " style="width:74vw; height:75vh;">
            </div>
        </v-sheet>

    </div>
</div>
</template>

<script>
export default {

}
</script>

<style>
.line {
    border: 2px solid rgb(221, 185, 185);
}
</style>
