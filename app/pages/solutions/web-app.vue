<template>
  <Cursor />
  <ProgressScroll />
  <Lines />
  <Navbar />
  <div id="smooth-wrapper">
    <div id="smooth-content">
      <main class="main-bg">
        <Header />
        <Services />
        <Process />
        <Services2 />
        <FAQS />
        <WorkShowcase category="web-app" />
      </main>
      <Footer />
    </div>
  </div>
</template>
<script setup>
import Footer from '@/components/light/modern-agency/Footer';
import Lines from '@/components/light/common/Lines';
import ProgressScroll from '@/components/light/common/ProgressScroll';
import Cursor from '@/components/light/common/cusor';
import Navbar from '@/components/light/creative-agency/Navbar';
import Header from '@/components/light/services-details/Header';
import Services from '@/components/light/services-details/Services';
import Process from '@/components/light/services-details/Process';
import Services2 from '@/components/light/services-details/Services2';
import FAQS from '@/components/light/services-details/FAQS';
import WorkShowcase from '@/components/light/solutions/WorkShowcase';
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
