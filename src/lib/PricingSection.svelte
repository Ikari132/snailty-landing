<script lang="ts">
	import {
		Jumbotron,
		Container,
		Row,
		Col,
		Card,
		CardBody,
		Button,
		ListGroup,
		ListGroupItem,
		CardDeck,
		CardFooter,
		CardHeader
	} from 'sveltestrap';
	import Anchor from './Anchor.svelte';
	import FaCheck from 'svelte-icons/fa/FaCheck.svelte';

	const freeVersionItems = [
		'20 teas',
		'Basic description of tea',
		'5 teawares',
		'5 articles every month',
		'Local data storage'
	];

	const proVersionItems = [
		'Unlimited teas',
		'Detailed tea testing',
		'Unlimited teawares',
		'Access to all articles',
		'Cloud data storage and access from different devices',
		'Access to the private tea club'
	];
</script>

<Jumbotron class="pricing-section-wrapper">
	<Container class="pricing-section">
		<Anchor id="pricing" />
		<Row class="mb-5">
			<Col>
				<h1 class="text-center">Pricing</h1>
			</Col>
		</Row>
		<Row class="justify-content-center">
			<CardDeck>
				<Card>
					<CardHeader class="text-center text-secondary bg-transparent" tag="h3">Free</CardHeader>
					<CardBody>
						<ListGroup flush>
							{#each freeVersionItems as item}
								<ListGroupItem class="d-flex align-items-center ">
									<div class="snailty-icon snailty-icon-lg snailty-icon-primary mr-2">
										<FaCheck />
									</div>
									{item}
								</ListGroupItem>
							{/each}
						</ListGroup>
					</CardBody>
					<CardFooter class="text-center bg-transparent">
						<Button color="secondary" outline>Try it</Button>
					</CardFooter>
				</Card>
				<Card>
					<CardHeader class="text-center text-primary bg-transparent" tag="h3">Pro</CardHeader>
					<CardBody>
						<ListGroup flush>
							{#each proVersionItems as item}
								<ListGroupItem class="d-flex align-items-center ">
									<div class="snailty-icon snailty-icon-lg snailty-icon-primary mr-2">
										<FaCheck />
									</div>
									{item}
								</ListGroupItem>
							{/each}
						</ListGroup>
					</CardBody>
					<CardFooter class="text-center bg-transparent">
						<Button color="primary" href="#contact">Get free Pro</Button>
					</CardFooter>
				</Card>
			</CardDeck>
		</Row>
	</Container>
</Jumbotron>

<style lang="scss">
</style>
