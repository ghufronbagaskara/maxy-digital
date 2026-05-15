<template>
  <Cursor />
  <ProgressScroll />
  <Lines />
  <div id="smooth-wrapper">
    <Navbar />
    <div id="smooth-content">
      <main class="main-bg">
        <Header />
        <Intro />
        <Marquee />
        <Intro2 />
      </main>
      <Footer />
    </div>
  </div>
</template>
<script setup>
import Footer from '@/components/light/blog-list/Footer';
import Header from '@/components/light/about/Header';
import Lines from '@/components/light/common/Lines';
import ProgressScroll from '@/components/light/common/ProgressScroll';
import Cursor from '@/components/light/common/cusor';
import Navbar from '@/components/light/creative-agency/Navbar';
import Intro from '@/components/light/about/Intro';
import Marquee from '@/components/light/about/Marquee';
import Intro2 from '@/components/light/about/Intro2';
import { onMounted } from 'vue';

onMounted(() => {
  gsap.registerPlugin(ScrollTrigger, ScrollSmoother);
  ScrollTrigger.normalizeScroll(true);
  ScrollSmoother.create({
    smooth: 2,
    effects: true,
  });
});
</script>
