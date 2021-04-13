<script lang="ts">
	import Logo from '$lib/Logo.svelte';
	import FlagIcon from '$lib/FlagIcon.svelte';
	import {
		Collapse,
		Navbar,
		NavbarToggler,
		NavbarBrand,
		Nav,
		NavItem,
		NavLink,
		UncontrolledDropdown,
		DropdownToggle,
		DropdownMenu,
		DropdownItem,
		Button
	} from 'sveltestrap';

	let isOpen = false;

	function handleUpdate(event) {
		isOpen = event.detail.isOpen;
	}
</script>

<main>
	<Navbar color="light" light expand="md" fixed="top">
		<NavbarBrand href="/">
			<Logo height={50} />
		</NavbarBrand>
		<NavbarToggler on:click={() => (isOpen = !isOpen)} />
		<Collapse {isOpen} navbar expand="md" on:update={handleUpdate}>
			<Nav class="ml-auto flex" navbar>
				<NavItem class="mx-1">
					<NavLink href="#about">About</NavLink>
				</NavItem>
				<NavItem class="mx-1">
					<NavLink href="#features">Features</NavLink>
				</NavItem>
				<NavItem class="mx-1">
					<NavLink href="#pricing">Pricing</NavLink>
				</NavItem>
				<NavItem class="mx-1">
					<NavLink href="#contact">Contact us</NavLink>
				</NavItem>
				<UncontrolledDropdown nav inNavbar>
					<DropdownToggle nav caret class="d-flex align-items-center">
						<FlagIcon flag="EN" />
					</DropdownToggle>
					<DropdownMenu right color="secondary">
						<DropdownItem>
							<div class="d-flex align-items-center">
								<FlagIcon flag="EN" />
								<div class="ml-3">English</div>
							</div>
						</DropdownItem>
						<DropdownItem>
							<div class="d-flex align-items-center">
								<FlagIcon flag="RU" />
								<div class="ml-3">Русский</div>
							</div>
						</DropdownItem>
					</DropdownMenu>
				</UncontrolledDropdown>
				<NavItem class="ml-2">
					<Button class="px-4" outline color="primary">Get free Pro</Button>
				</NavItem>
			</Nav>
		</Collapse>
	</Navbar>

	<h2>Your guide to the world of tea</h2>

	<a href="https://app.snailty.com">
		<Button color="primary">Open app</Button>
	</a>
</main>

<style lang="scss">
	main {
		text-align: center;
		padding-top: 100px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4rem;
		font-weight: 100;
		line-height: 1.1;
		margin: 4rem auto;
		max-width: 14rem;
	}

	@media (min-width: 480px) {
		h1 {
			max-width: none;
		}
	}
</style>
