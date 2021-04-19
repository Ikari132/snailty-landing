<script lang="ts">
	import { Jumbotron, Container, Row, Col } from 'sveltestrap';
	import Anchor from './Anchor.svelte';
	import FaAward from 'svelte-icons/fa/FaAward.svelte';
	import FaLeaf from 'svelte-icons/fa/FaLeaf.svelte';
	import FaBoxes from 'svelte-icons/fa/FaBoxes.svelte';
</script>

<Jumbotron class="features-section-wrapper snailty-full-height">
	<Container class="features-section">
		<Anchor id="features" />
		<Row class="mb-5">
			<Col>
				<h1 class="text-center">Manage your tea easily</h1>
			</Col>
		</Row>
		<Row>
			<!-- TODO: кейсы получше, иконки тож, текста посочнее -->
			<Col md="4" class="text-center mb-4">
				<div class="icon-wrapper mx-auto mb-4">
					<FaAward />
				</div>
				<h4>Recommendations</h4>
				<p>Get perfect tea for your mood</p>
			</Col>
			<Col md="4" class="text-center mb-4">
				<div class="icon-wrapper mx-auto mb-4">
					<FaLeaf />
				</div>
				<h4>Available tea</h4>
				<p>Always be aware of what kind of tea you have in stock</p>
			</Col>
			<Col md="4" class="text-center mb-4">
				<div class="icon-wrapper mx-auto mb-4">
					<FaBoxes />
				</div>
				<h4>Кeep your teas in order</h4>
				<p>Be aware of which teas you might have forgotten</p>
			</Col>
		</Row>
	</Container>
</Jumbotron>

<style lang="scss">
	:global(.features-section-wrapper) {
		background: linear-gradient(90deg, rgb(139, 209, 250), rgb(253, 232, 191), rgb(255, 198, 197));
	}

	:global(.features-section-wrapper) {
		position: relative;
		background-size: 100%;
		background-repeat: no-repeat;
		background-position: top;
		background-image: url("data:image/svg+xml,%3C%3Fxml version='1.0' standalone='no'%3F%3E%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1440 320'%3E%3Cdefs%3E%3ClinearGradient id='gradient' x2='579.43' y1='215.83' y2='215.83' gradientTransform='scale(2.4852 .40238)' gradientUnits='userSpaceOnUse'%3E%3Cstop stop-color='%238bd1fa' offset='0'/%3E%3Cstop stop-color='%23fde8bf' offset='.5'/%3E%3Cstop stop-color='%23ffc6c5' offset='1'/%3E%3C/linearGradient%3E%3Cstyle type='text/css'%3E%3C!%5BCDATA%5B path %7B fill: url(%23gradient); %7D %5D%5D%3E%3C/style%3E%3C/defs%3E%3Cpath fill='%230099ff' fill-opacity='1' d='M0,0L120,10.7C240,21,480,43,720,42.7C960,43,1200,21,1320,10.7L1440,0L1440,0L1320,0C1200,0,960,0,720,0C480,0,240,0,120,0L0,0Z'%3E%3C/path%3E%3C/svg%3E");
	}

	.icon-wrapper {
		width: 100px;
		height: 100px;
	}
</style>
