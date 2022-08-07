<script>
export default {
  name: 'Setup',
  data() {
    return {
      category: '',
      difficulty: '',
      type: '',
      showSetup: true,
    };
  },
  created() {
    this.getData();
    console.log(this.value);
  },
  methods: {
    getData() {
      fetch(`https://opentdb.com/api.php?amount=13`)
        .then((result) => {
          return result.json();
        })
        .then((results) => {
          console.log(results);
        });
    },
    start() {
      const element = document.querySelector('.setup-container');
      element.style['-webkit-animation'] = 'animRight .3s forwards';
      setTimeout(() => {
        this.$router.push({
          name: 'Question',
        });
      }, 500);
    },
  },
};
</script>

<style lang="scss" scoped>
@import '../styles/main.scss';
.setup-container {
  .top-img {
    margin-bottom: 25px;
    text-align: center;
  }
  div {
    margin: 10px 0;
  }
  div select,
  div input {
    width: 250px;
    height: 40px;
    border: 1px solid #d9d9d9;
    border-radius: 10px;
    padding-left: 10px;
    font-size: 16px;
    &:focus {
      outline: none;
    }
  }
  div button {
    width: 250px;
    margin-top: 20px;
    border: 0;
    border-radius: 20px;
    padding: 10px;
    background: #3fd8f3;
    color: #ffffff;
    transition: 0.5s;
    &:hover {
      background: #0eb9d8;
    }
  }
}
