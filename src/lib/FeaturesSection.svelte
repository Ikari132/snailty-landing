<script lang="ts">
	import { Jumbotron, Container, Row, Col } from 'sveltestrap';
	import Anchor from './Anchor.svelte';
	import FaAward from 'svelte-icons/fa/FaAward.svelte';
	import FaLeaf from 'svelte-icons/fa/FaLeaf.svelte';
	import FaBoxes from 'svelte-icons/fa/FaBoxes.svelte';
</script>

<Jumbotron class="features-section-wrapper">
	<Container class="features-section">
		<Anchor id="features" />
		<Row class="mb-5">
			<Col>
				<h1 class="text-center">Manage your tea easily</h1>
			</Col>
		</Row>
		<Row>
			<!-- TODO: кейсы получше, иконки тож, текста посочнее -->
			<Col md="4" class="text-center mb-4 mb-md-0">
				<div class="icon-wrapper mx-auto mb-4">
					<FaAward />
				</div>
				<h4>Recommendations</h4>
				<p>Get perfect tea for your mood</p>
			</Col>
			<Col md="4" class="text-center mb-4 mb-md-0">
				<div class="icon-wrapper mx-auto mb-4">
					<FaLeaf />
				</div>
				<h4>Available tea</h4>
				<p>Always be aware of what kind of tea you have in stock</p>
			</Col>
			<Col md="4" class="text-center mb-4 mb-md-0">
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
	.icon-wrapper {
		width: 100px;
		height: 100px;
	}
</style>
