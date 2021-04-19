<script lang="ts">
	import { Jumbotron, Container, Row, Col } from 'sveltestrap';
	import Anchor from './Anchor.svelte';
</script>

<Jumbotron class="club-section-wrapper">
	<Container class="club-section">
		<Anchor id="club" />
		<Row>
			<Col sm="12" md="6" class="my-md-auto mb-4">
				<h4 class="text-center">
					Get access to a private tea club and share your hobby with others!
				</h4>
			</Col>
			<Col sm="12" md="6">
				<!-- <div class="share-tea" /> -->
				<img src="/sharing.png" class="image-share img-fluid mb-3" alt="share" />
			</Col>
		</Row>
	</Container>
</Jumbotron>

<style lang="scss">
	.share-tea {
		background: url('/sharing.png');
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
		height: calc(100vh - 210px);
		width: 100%;
	}
</style>
