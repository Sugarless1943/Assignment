<template>
    <div class="home-nav">
      <header>
        Assignment
      </header>
      <main>
        <ul>
          <li v-for="item in tags" :key="item.name" @click="to(item.name)">{{ item.name }}</li>
        </ul>
      </main>
    </div>
   
</template>

<script>
export default {
    name: "Nav",
    data() {
        return {
          tags: [
            {
              name: 'part1'
            },
            {
              name: 'part2'
            }
          ]
        }
    },

    methods: {
      to(name) {
        this.$router.push({path: name})
      }
    }
}
</script>

<style lang="scss" scoped>
  .home-nav {
    display: flex;
    flex-direction: column;
    height: 100%;
    border-right: 1px solid #ccc;

    &>header {
      height: 60px;
      line-height: 60px;
      font-weight: bold;
    }

    &>main {
      flex: 1;
      & > ul {
        display: flex;
        flex-direction: column;
        padding: 0;
        margin: 0;
        li {
          height: 50px;
          line-height: 50px;

          &:hover {
            cursor: pointer;
            color: #53A1FC; 
          }
        }
      }
    }

   
  }
</style>