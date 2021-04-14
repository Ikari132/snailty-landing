<script lang="ts">
	import {
		Col,
		Container,
		Row,
		Input,
		Button,
		InputGroup,
		InputGroupAddon,
		Jumbotron
	} from 'sveltestrap';
	import Anchor from './Anchor.svelte';
</script>

<Jumbotron class="intro-section-wrapper">
	<Container class="intro-section">
		<Anchor id="home" />
		<Row>
			<Col sm="12" md="6" class="my-auto">
				<h1 class="text-sm-center text-md-left pb-4">All your teas in one App</h1>
				<p class="text-sm-center text-md-left text-secondary">
					Personalized recommendations, infusion timer, session history, and simple tea management
					will allow you to fully enjoy your hobby.
				</p>
				<InputGroup>
					<Input class="snailty-input-with-button" placeholder="mail@example.com" />
					<InputGroupAddon addonType="append">
						<Button color="primary">Get free Pro</Button>
					</InputGroupAddon>
				</InputGroup>
			</Col>
			<Col sm="12" md="6">
				<div class="d-flex flex-column align-items-center">[PHONE PREVIEW]</div>
			</Col>
		</Row>
	</Container>
</Jumbotron>

<style lang="scss">
	:global(.intro-section .snailty-input-with-button) {
		max-width: 200px;
	}

	:global(.intro-section-wrapper) {
		background: linear-gradient(20deg, #f5fbf9 50%, #fff 50%);
	}
</style>
