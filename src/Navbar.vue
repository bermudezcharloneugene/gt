<template>
  <div >
  <nav class="nav justify-content-center">
    <a class="nav-link active" href="#about">About</a>
    <a class="nav-link disabled" href="">Disabled link</a>
  </nav>
  </div>
</template>

<script>
export default {
	name: 'Navbar',
	data() {
		return {
			navColor: 'navbar-dark bg-transparent',
		}
	},
  created () {
    window.addEventListener('scroll', this.calcScroll);
  },
  destroyed  () {
    window.removeEventListener('scroll', this.calcScroll);
  },
  methods: {
    calcScroll() {
			if(window.scrollY >= 200) 
			{
				this.navColor = 'navbar-dark bg-dark';
			}else {
				this.navColor = 'navbar-dark bg-transparent';
			}
    }
  }
}
</script>

<style scoped>
		.nav-text {
			font-size: 16px;
			color: white;
		}
		.nav-text:hover {
			background: white;
			color: black;
			padding: .3em;
			border-radius: 20%;
		}
		.navbar-brand {
			text-shadow: 0px 0px 3px black;
		}
		.navbar-brand:hover {
			text-shadow: 0px 0px 3px black;
			background: rgba(145, 143, 143, 0.521);
			padding: .2em;
			border-top-left-radius: 30%;
			border-bottom-right-radius: 30%;
		}
		.bg-dark {
			transition: .8s;
			background-color: rgb(0, 0, 0)!important;
		}

		.bg-transparent {
			transition: .8s;
			background-color: rgba(0,0,0,0)!important;
		}
</style>