<template>
    <div class="home-nav">
      <header>
        Assignment
      </header>
      <main>
        <ul>
          <li>part1</li>
          <li>part2</li>
        </ul>
      </main>
    </div>
   
</template>

<script>
export default {
    name: "Nav",
    data() {
        return {
          
        }
    }
}
</script>

<style lang="scss" scoped>
  .home-nav {
    &>header {
      height: 60px;
      line-height: 60px;
      font-weight: bold;
    }

    ul {
      display: flex;
      flex-direction: column;
      padding: 0;
    }
  }
</style>