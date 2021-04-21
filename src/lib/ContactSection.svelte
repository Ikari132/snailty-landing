<script lang="ts">
	import {
		Jumbotron,
		Container,
		Row,
		Col,
		Card,
		CardTitle,
		CardBody,
		Button,
		CardText,
		InputGroup,
		InputGroupAddon,
		Input
	} from 'sveltestrap';
	import Anchor from './Anchor.svelte';
</script>

<Jumbotron class="contact-section-wrapper">
	<Container class="contact-section">
		<Anchor id="contact" />
		<Row class="justify-content-center">
			<Col md="8">
				<Card class="my-5">
					<CardBody class="text-center p-md-5">
						<CardTitle><h1>Stay up to date</h1></CardTitle>
						<CardText class="mb-4">
							Leave your mail and be the first to know about the release of the application, and
							also get a free Pro version for 3 months!
						</CardText>
						<InputGroup class="justify-content-center">
							<Input class="snailty-input-with-button" placeholder="mail@example.com" />
							<InputGroupAddon addonType="append">
								<Button color="primary">Get free Pro</Button>
							</InputGroupAddon>
						</InputGroup>
					</CardBody>
				</Card>
			</Col>
		</Row>
	</Container>
</Jumbotron>

<style lang="scss">
	:global(.contact-section .snailty-input-with-button) {
		max-width: 300px;
	}

	:global(.contact-section-wrapper) {
		background-image: url('/contact.jpg');
		background-position: 50% 50%;
		background-repeat: no-repeat;
		background-size: cover;
	}
</style>
