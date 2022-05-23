<template>
    <h1> Attribute Binding</h1>
    <h1 v-bind:class="titleClass">Color converted into "Red"</h1> <!--adding class from the script-->
    <p v-bind:id="paraID">Lorem ipsum dolor sit amet consectetur adipisicing elit. Sapiente quisquam hic numquam aspernatur illo! Eaque excepturi et culpa enim deserunt quos eveniet cumque sunt. Facilis impedit atque sit expedita veritatis.</p>
</template>
<script>
export default{
        name:'AttributeBinding',
        data(){

            return{
            titleClass: 'title',
            paraID:'para'
            }
        }
    }
</script>
<style>
.title{
    color:red;
}
#para{
    font-style: italic;
}
</style>