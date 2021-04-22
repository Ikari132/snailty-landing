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

<Jumbotron class="intro-section-wrapper snailty-full-height">
	<Anchor id="home" />
	<Container class="intro-section">
		<Row>
			<Col sm="12" md="6" class="my-md-auto mb-4 text-light">
				<h1 class="text-center text-md-left pb-3">All your teas in one App</h1>
				<p class="text-center text-md-left pb-3">
					Personalized recommendations, infusion timer, session history, and simple tea management
					will allow you to fully enjoy your hobby.
				</p>
				<InputGroup class="justify-content-center justify-content-md-start">
					<Input class="snailty-input-with-button" placeholder="mail@example.com" />
					<InputGroupAddon addonType="append">
						<Button color="secondary">Get free Pro</Button>
					</InputGroupAddon>
				</InputGroup>
			</Col>
			<Col sm="12" md="6">
				<div class="app-in-phone" />
			</Col>
		</Row>
	</Container>
</Jumbotron>

<style lang="scss">
	@import 'node_modules/bootstrap/scss/mixins';
	@import 'node_modules/bootstrap/scss/functions';
	@import 'node_modules/bootstrap/scss/variables';

	@import './../constants.scss';

	.app-in-phone {
		background: url('/app1.png');
		animation: app-in-phone-animation 10s infinite;
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
		min-height: calc(100vh - 204px);
		width: 100%;
		height: 100%;
	}

	@keyframes app-in-phone-animation {
		0% {
			background-image: url('/app1.png');
		}
		50% {
			background-image: url('/app2.png');
		}
		100% {
			background-image: url('/app1.png');
		}
	}

	:global(.intro-section .snailty-input-with-button) {
		max-width: 200px;
	}

	// NOTE: intro-section-wrapper -> app.scss

	@include media-breakpoint-only(xs) {
		:global(.intro-section-wrapper) {
			background-image: url('/spyral_mobile.png');
		}
	}
</style>
