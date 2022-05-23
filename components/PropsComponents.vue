<template>
    <h1>Props</h1>
    <h3>{{msg || "No props passed yet"}}</h3>
</template>
<script>
export default{
    name: 'ChildComponent',
    props:{
        msg: String
    }
}
</script>