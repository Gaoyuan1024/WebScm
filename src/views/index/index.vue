<template>
  <div class="index-container"></div>
</template>
<script>
export default {
  name: 'Index',
  data() {
    return {
      // svg
      title: '全国',
      size: 5000,
      angle: 0,
      items: [
        { name: '广州市', num: 88 },
        { name: '深圳市', num: 85 },
        { name: '东莞市', num: 82 },
        { name: '香港', num: 79 },
        { name: '佛山市', num: 76 },
        { name: '中山市', num: 74 },
        { name: '江门市', num: 72 },
        { name: '澳门', num: 68 },
        { name: '江门市', num: 68 },
        { name: '江门市', num: 68 },
        { name: '江门市', num: 68 },
      ],
      svgStyle: {
        strokeWidth: 5,
        stroke: '#E3E6ED',
      },
    }
  },
  computed: {
    topHeight() {
      // 20% of the size
      return this.size * 0.2
    },
    bottomHeight() {
      // 80% of the size
      return this.size * 0.4
    },
    width() {
      return this.size
    },
    halfSize() {
      // 50% of the size
      return this.size * 0.5
    },
    distance() {
      // distance between two array items on the horizon
      return Math.round(this.width / this.items.length)
    },
    // xPosition() {
    //   return i => {
    //      return this.distance * i + this.distance * 0.5
    //   };
    // },
    radius() {
      return this.topHeight * 0.3
    },
    viewbox() {
      return '0 0 ' + this.size + ' ' + this.size * 0.5
    },
  },
  created() {},
  mounted() {},
  methods: {},
}
</script>
