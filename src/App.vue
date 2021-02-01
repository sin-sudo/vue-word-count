<template>
  <div class='entire'>
    <h2 class='title'>レポート何文字書いた？</h2>
    <div class="textarea">
      <v-textarea
        solo
        name="input-7-4"
        label="数えたい文字列を入力してください"
        v-model.trim='words'
      ></v-textarea>
    </div>
    <div class="result">
      <p id='count'>文字数: {{ wordLength }}</p>
      <v-btn elevation="2" @click='reset'>リセット</v-btn>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      words: ''
    }
  },
  computed: {
    wordLength() {
      return this.words.length
    }
  },
  methods: {
    reset() {
      this.words = ''
    }
  }
}
</script>

<style scoped>
.entire {
  font-family: 'Slabo 27px', serif;
}

.title {
  text-align: center;
  padding: 30px;
}

.textarea {
  width: 400px;
  margin: 0 auto;
}

.result {
  text-align: center;
}

#count {
  margin: 10px;
}
</style>