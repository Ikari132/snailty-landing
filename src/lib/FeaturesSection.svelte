<script lang="ts">
	import { Jumbotron, Container, Row, Col } from 'sveltestrap';
	import Anchor from './Anchor.svelte';
</script>

<Jumbotron class="features-section-wrapper">
	<Container class="features-section">
		<Anchor id="features" />
		<Row class="mb-5">
			<Col>
				<h1 class="text-center">Manage your tea</h1>
			</Col>
		</Row>
		<Row>
			<!-- TODO: кейсы получше, иконки тож, текста посочнее -->
			<Col md="4" class="text-center mb-4 mb-md-0">
				<img src="/teas.png" class="img-fluid mb-3" alt="Recommendations" />
				<h4>Recommendations</h4>
				<p>Get perfect tea for your mood</p>
			</Col>
			<Col md="4" class="text-center mb-4 mb-md-0">
				<img src="/notea.png" class="img-fluid mb-3" alt="Available tea" />
				<h4>Available tea</h4>
				<p>Always be aware of what kind of tea you have in stock</p>
			</Col>
			<Col md="4" class="text-center mb-4 mb-md-0">
				<img src="/teashelf.png" class="img-fluid mb-3" alt="Кeep your teas in order" />
				<h4>Кeep your teas in order</h4>
				<p>Be aware of which teas you might have forgotten</p>
			</Col>
		</Row>
	</Container>
</Jumbotron>

<style lang="scss">
</style>
