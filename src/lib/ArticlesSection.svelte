<script lang="ts">
	import { Jumbotron, Container, Row, Col } from 'sveltestrap';
	import Anchor from './Anchor.svelte';
</script>

<Jumbotron class="articles-section-wrapper bg-light">
	<Container class="articles-section">
		<Anchor id="articles" />
		<Row class="mb-3">
			<Col class="text-center">
				<h1>Articles</h1>
				<p>Learn a lot about tea, its history, health benefits and brewing methods</p>
			</Col>
		</Row>
		<Row>
			<Col sm="6" md="3" class="text-center mb-5">
				<img src="/teaware.jpg" class="article-image img-fluid mb-3" alt="teaware" />
				<h4>Teaware</h4>
			</Col>
			<Col sm="6" md="3" class="text-center mb-5">
				<img src="/sorts.jpg" class="article-image img-fluid mb-3" alt="sorts" />
				<h4>Sorts of tea</h4>
			</Col>
			<Col sm="6" md="3" class="text-center mb-5">
				<img src="/history.jpg" class="article-image img-fluid mb-3" alt="history" />
				<h4>Tea history</h4>
			</Col>
			<Col sm="6" md="3" class="text-center mb-5">
				<img src="/health.jpg" class="article-image img-fluid mb-3" alt="health" />
				<h4>Health benefits</h4>
			</Col>
		</Row>
	</Container>
</Jumbotron>

<style lang="scss">
	.article-image {
		max-height: 350px;
		border-radius: 20px;
	}
</style>
