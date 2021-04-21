<script lang="ts">
	import { Container, Row, Col } from 'sveltestrap';
	import Logo from '$lib/Logo.svelte';
	import FaInstagram from 'svelte-icons/fa/FaInstagram.svelte';
	import FaTwitter from 'svelte-icons/fa/FaTwitter.svelte';
</script>

<footer>
	<Container fluid class="bg-dark text-light">
		<Row class="px-1 py-3">
			<Col sm="6" class="text-center text-sm-left mb-1 mb-sm-0">
				<Logo
					height={50}
					type="light"
					class="mb-2 justify-content-center justify-content-sm-start"
				/>
				© 2021 Snailty.com
			</Col>
			<Col sm="6" class="text-center text-sm-right">
				<div class="d-flex justify-content-center justify-content-sm-end my-1">
					<a
						class="icon-wrapper text-light d-flex ml-2"
						href="https://www.instagram.com/mrteasnail/"
						target="_blank"
					>
						<FaInstagram />
					</a>
					<a
						class="icon-wrapper text-light d-flex ml-2"
						href="https://twitter.com/MrTeaSnail"
						target="_blank"
					>
						<FaTwitter />
					</a>
				</div>
				<a href="mailto:info@snailty.com" class="text-light">info@snailty.com</a>
				<div>
					<a href="/#" class="text-light">Legal</a>
					|
					<a href="/#" class="text-light">Privacy Policy</a>
				</div>
			</Col>
		</Row>
	</Container>
</footer>

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

	.icon-wrapper {
		width: 25px;
		height: 25px;
	}
</style>
