<template>
  <div class="share">
    <p>シェア</p>
    <textarea></textarea>
    <div>
      <button>シェアする</button>
    </div>
  </div>
</template>

<style scoped>
.share{
  margin: 15px;
}
.share textarea{
  width: 100%;
  height: 120px;
  margin-top: 15px;
  margin-bottom: 15px;
  border-radius: 15px;
  background-color: #15202b;
  color: white;
  border: 1px solid white;
  resize: none;
}
button{
  width: 100px;
  color: white;
  background-color: #5419da;
  border-radius: 15px;
  display: block;
  margin: 0 0 0 auto;
}
</style>