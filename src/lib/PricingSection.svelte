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
		ListGroup,
		ListGroupItem
	} from 'sveltestrap';
	import Anchor from './Anchor.svelte';
</script>

<Jumbotron class="pricing-section-wrapper">
	<Container class="pricing-section">
		<Anchor id="pricing" />
		<Row class="mb-5">
			<Col>
				<h1 class="text-center">Pricing</h1>
			</Col>
		</Row>
		<Row>
			<Col md="6" class="mb-5">
				<Card>
					<CardBody class="text-center">
						<CardTitle><h3 class="text-secondary">Free</h3></CardTitle>
						<ListGroup class="mb-4">
							<!-- TODO: add items -->
							<ListGroupItem>Item</ListGroupItem>
							<ListGroupItem>Item</ListGroupItem>
							<ListGroupItem>Item</ListGroupItem>
							<ListGroupItem>-</ListGroupItem>
							<ListGroupItem>-</ListGroupItem>
						</ListGroup>
						<Button color="secondary" outline>Try it</Button>
					</CardBody>
				</Card>
			</Col>
			<Col md="6">
				<Card>
					<CardBody class="text-center">
						<CardTitle><h3 class="text-primary">Pro</h3></CardTitle>
						<ListGroup class="mb-4">
							<ListGroupItem>Item</ListGroupItem>
							<ListGroupItem>Item</ListGroupItem>
							<ListGroupItem>Item</ListGroupItem>
							<ListGroupItem>Item</ListGroupItem>
							<ListGroupItem>Item</ListGroupItem>
						</ListGroup>
						<Button color="primary">Get free Pro</Button>
					</CardBody>
				</Card>
			</Col>
		</Row>
	</Container>
</Jumbotron>

<style lang="scss">
</style>
