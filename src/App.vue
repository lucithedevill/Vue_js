<template>
  <div>
    <MyHeader appName="Laptop Outlet" authorName="Surya Naga Anil Kumar Midde" />
    <LaptopBox :laptops="laptops" />
  </div>
</template>
<script>
import MyHeader from '@/components/MyHeader.vue';
import LaptopBox from '@/components/LaptopBox.vue';
export default {
  name: 'App',
  components: {
    MyHeader,
    LaptopBox,
  },
  data() {
    return {
      laptops: []
    };
  },
  methods: {
    async fetchLaptops() {
      try {
        const res = await fetch('https://node-mkvm.onrender.com/api');
        if (!res.ok) {
          throw new Error(`Failed to fetch  the laptops: ${res.statusText}`);
        }
        const data = await res.json();
        return data;
      } catch (error) {
        console.error('Error fetching laptops:', error);
        return [];
      }
    }
  },
  async created() {
    this.laptops = await this.fetchLaptops();
  }
};
</script>
