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
	<Anchor id="home" />
	<Container class="intro-section">
		<Row>
			<Col sm="12" md="6" class="my-md-auto mb-4">
				<h1 class="text-center text-md-left pb-4">All your teas in one App</h1>
				<p class="text-center text-md-left text-secondary">
					Personalized recommendations, infusion timer, session history, and simple tea management
					will allow you to fully enjoy your hobby.
				</p>
				<InputGroup class="justify-content-center justify-content-md-start">
					<Input class="snailty-input-with-button" placeholder="mail@example.com" />
					<InputGroupAddon addonType="append">
						<Button color="primary">Get free Pro</Button>
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

	.app-in-phone {
		background: url('/app_day.png');
		animation: app-in-phone-animation 30s infinite;
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
		height: calc(100vh - 210px);
		width: 100%;
	}

	@keyframes app-in-phone-animation {
		0% {
			background-image: url('/app_day.png');
		}
		25% {
			background-image: url('/app_evening.png');
		}
		50% {
			background-image: url('/app_night.png');
		}
		75% {
			background-image: url('/app_morning.png');
		}
		100% {
			background-image: url('/app_day.png');
		}
	}

	:global(.intro-section .snailty-input-with-button) {
		max-width: 200px;
	}

	:global(.intro-section-wrapper) {
		position: relative;
		background-size: 100%;
		background-repeat: no-repeat;
		background-position: bottom;
		background-image: url("data:image/svg+xml,%3C%3Fxml version='1.0' standalone='no'%3F%3E%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1440 320'%3E%3Cdefs%3E%3ClinearGradient spreadMethod='pad' id='gradient' x1='0%25' y1='0%25' x2='100%25' y2='0%25'%3E%3Cstop offset='0%25' style='stop-color:rgb(139, 209, 250);stop-opacity:1;' /%3E%3Cstop offset='50%25' style='stop-color:rgb(253, 232, 191);stop-opacity:1;' /%3E%3Cstop offset='100%25' style='stop-color:rgb(255, 198, 197);stop-opacity:1;' /%3E%3C/linearGradient%3E%3Cstyle type='text/css'%3E%3C!%5BCDATA%5B path %7B fill: url(%23gradient); %7D %5D%5D%3E%3C/style%3E%3C/defs%3E%3Cpath fill-opacity='1' d='M0,320L48,282.7C96,245,192,171,288,128C384,85,480,75,576,101.3C672,128,768,192,864,192C960,192,1056,128,1152,112C1248,96,1344,128,1392,144L1440,160L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z'%3E%3C/path%3E%3C/svg%3E");
	}

	@include media-breakpoint-only(sm) {
		:global(.intro-section-wrapper) {
			background-image: url("data:image/svg+xml,%3Csvg width='606.84' height='320' version='1.1' viewBox='0 0 606.84 320' xmlns='http://www.w3.org/2000/svg'%3E%3Cdefs%3E%3ClinearGradient spreadMethod='pad' id='gradient' x1='0%25' y1='0%25' x2='100%25' y2='0%25'%3E%3Cstop offset='0%25' style='stop-color:rgb(139, 209, 250);stop-opacity:1;' /%3E%3Cstop offset='50%25' style='stop-color:rgb(253, 232, 191);stop-opacity:1;' /%3E%3Cstop offset='100%25' style='stop-color:rgb(255, 198, 197);stop-opacity:1;' /%3E%3C/linearGradient%3E%3Cstyle type='text/css'%3E%3C!%5BCDATA%5B path %7B fill: url(%23gradient); %7D %5D%5D%3E%3C/style%3E%3C/defs%3E%3Cpath d='m461.41 107.64c-17.684 0.04688-35.684 1.3594-53.684 4.3594-96 16-192 80-288 80-39.909 0-79.818-11.075-119.73-25.918v153.92h606.84v-189.01c-39.256-11.57-90.82-23.494-145.43-23.35z' fill='url(%23gradient)'/%3E%3C/svg%3E%0A");
		}
	}

	@include media-breakpoint-only(xs) {
		:global(.intro-section-wrapper) {
			background-image: none;
		}
	}
</style>
