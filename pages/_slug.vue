<template>
  <div>
    <div>
     {{ category.name }}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slug: this.$route.params.slug,
      categories: [
        { slug: 'geography', name: 'Geography', color: 'rgb(66, 153, 225)' },
        { slug: 'history', name: 'History', color: 'rgb(236, 201, 75)' },
        { slug: 'sports', name: 'Sports', color: 'rgb(237, 137, 54)' },
      ]
    }
  },

  computed: {
    category() {
      return this.categories.find(c => c.slug === this.slug) || {}
    }
  },

  head() {
    return {
      title: this.category.name,
      link: [
        {
          rel: 'icon',
          type: 'image/svg+xml',
          href: `data:image/svg+xml,
                <svg
                  width="32"
                  height="32"
                  viewBox="0 0 32 32"
                  fill="none"
                  style="color: ${this.category.color};"
                  xmlns="http://www.w3.org/2000/svg"
                ><circle cx="16" cy="16" r="15.0049" fill="currentColor" /></svg>`,
        },
      ],
    }
  }
}
</script>
