<script lang="ts">
	import { Jumbotron, Container, Row, Col } from 'sveltestrap';
	import Anchor from './Anchor.svelte';
</script>

<Jumbotron class="about-section-wrapper snailty-full-height">
	<Container class="about-section">
		<Anchor id="about" />
		<Row class="flex-column-reverse flex-md-row">
			<Col sm="12" md="6">
				<div class="app-in-phones" />
			</Col>
			<Col sm="12" md="6" class="my-md-auto mb-4">
				<h4 class="text-center">
					Our application will help you tidy up your teas, keep abreast of tea topics and make tea
					drinking more convenient and enjoyable.
				</h4>
			</Col>
		</Row>
	</Container>
</Jumbotron>

<style lang="scss">
	:global(.about-section-wrapper) {
		background: linear-gradient(90deg, rgb(139, 209, 250), rgb(253, 232, 191), rgb(255, 198, 197));
	}

	.app-in-phones {
		background: url('/app_multiple_screens.png');
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
		height: calc(100vh - 210px);
		width: 100%;
	}
</style>
