<style lang="scss">
 @import "@/assets/scss/style.scss"; 
</style>
<template>

    <div class="parent">
        <Navbar/>
        <Side/>
        <Millieu/>
        <Right/>
        <FooterLeft/>
        <FooterRight/>
        </div>

</template>

<script>
import Navbar from './Navbar.vue';
import Side from './Side.vue';
import Millieu from './Millieu.vue';
import Right from './Right.vue';
import FooterLeft from './FooterLeft.vue';
import FooterRight from './FooterRight.vue';
export default {
    name: "HelloWorld",
    props: {
        msg: String
    },
    components: { Navbar, Side, Millieu, Right, FooterLeft, FooterRight }
}
</script>
