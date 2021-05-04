<template>
  <div class="hadith">
    <h1>{{ msg }}</h1>
    <ol class="hadith-list">
      <li v-for="item in items" :key="item.id" class="hadith-list-item">
          <span class="name"><strong>Name:</strong> {{ item.name }}</span>
          <span class="description"><strong>Description:</strong> {{ item.description }}</span>
          <span class="references"><strong>References:</strong> {{ item.references }}</span>
          <span class="grade"><strong>Grade:</strong> {{ item.grade }}</span>
      </li>
    </ol>
  </div>
</template>

<script>
export default {
    // props: ['items'],
    name: 'HadithWorld',
    props: {
        msg: String,
        items: Array
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h1 {
        font-weight: 700;
    }
    .hadith {
        max-width: 900px;
        margin: 0 auto;
    }

    .hadith-list {
        /* list-style-type: none; */
        padding: 0;
        margin: 0;
    }

    .hadith-list li {
        border: 1px solid #666;
        padding: 10px 16px;
        border-radius: 5px;
        text-align: left;
        margin-bottom: 16px;
    }

    .hadith-list li:not(:last-child) {
        margin-bottom: 16px;
    }

    .hadith-list li > span {
        display: block;
        padding: 5px 0;
    }
</style>
