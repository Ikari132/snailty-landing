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
				<div class="app-in-phone" />
			</Col>
		</Row>
	</Container>
	<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320" class="jumbotron-wave">
		<defs>
			<linearGradient spreadMethod="pad" id="gradient" x1="0%" y1="0%" x2="100%" y2="0%">
				<stop offset="0%" style="stop-color:rgb(139, 209, 250);stop-opacity:1;" />
				<stop offset="50%" style="stop-color:rgb(253, 232, 191);stop-opacity:1;" />
				<stop offset="100%" style="stop-color:rgb(255, 198, 197);stop-opacity:1;" />
			</linearGradient>
		</defs>
		<path
			fill-opacity="1"
			d="M0,128L48,149.3C96,171,192,213,288,229.3C384,245,480,235,576,202.7C672,171,768,117,864,85.3C960,53,1056,43,1152,58.7C1248,75,1344,117,1392,138.7L1440,160L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"
		/>
	</svg>
</Jumbotron>

<style lang="scss">
	.app-in-phone {
		background: url('/app_day.png');
		animation: app-in-phone-animation 30s infinite;
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
		height: 450px;
		width: 100%;
	}

	@keyframes app-in-phone-animation {
		0% {
			background: url('/app_day.png');
			background-size: contain;
			background-repeat: no-repeat;
			background-position: center;
		}
		25% {
			background: url('/app_evening.png');
			background-size: contain;
			background-repeat: no-repeat;
			background-position: center;
		}
		50% {
			background: url('/app_night.png');
			background-size: contain;
			background-repeat: no-repeat;
			background-position: center;
		}
		75% {
			background: url('/app_morning.png');
			background-size: contain;
			background-repeat: no-repeat;
			background-position: center;
		}
		100% {
			background: url('/app_day.png');
			background-size: contain;
			background-repeat: no-repeat;
			background-position: center;
		}
	}

	.jumbotron-wave {
		position: absolute;
		bottom: 0;
		left: 0;
		z-index: -1;

		path {
			fill: url(#gradient);
		}
	}

	:global(.intro-section .snailty-input-with-button) {
		max-width: 200px;
	}

	:global(.intro-section-wrapper) {
		position: relative;
	}
</style>
