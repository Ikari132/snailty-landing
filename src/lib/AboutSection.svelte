<script lang="ts">
	import { Jumbotron, Container, Row, Col } from 'sveltestrap';
	import Anchor from './Anchor.svelte';
</script>

<Jumbotron class="about-section-wrapper bg-light">
	<Container class="about-section">
		<Anchor id="about" />
		<Row class="justify-content-center">
			<Col md="8">
				<h4 class="text-center" style="line-height: 40px;">
					Our application will help you tidy up your teas, keep abreast of tea topics and make tea
					drinking more convenient and enjoyable.
				</h4>
			</Col>
		</Row>
	</Container>
</Jumbotron>

<style lang="scss">
</style>
