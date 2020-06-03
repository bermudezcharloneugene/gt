<template>
    <div >
        <Header></Header>
        <first-parallax></first-parallax>
        <Content></Content>
        <second-parallax />
        <FooterInformation/>
    </div>
</template>

<script>
import Header from './Header';
import Content from './Content';
import FirstParallax from './FirstParallax';
import SecondParallax from './SecondParallax';
import FooterInformation from './FooterInformation';

export default {
    name: 'Home',
    components: {
        Header: Header,
        Content: Content,
        firstParallax: FirstParallax,
        secondParallax: SecondParallax,
        FooterInformation
    }
}
</script>

<style >
    .text-center {
        text-align: center;
    }

    .jumbotron {
        background: #000000;
        margin-bottom: 0px!important;
        border: 0px!important;
    }
</style>