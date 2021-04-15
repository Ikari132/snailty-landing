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
	import { APP_LINK } from './constants';

	let isMenuOpen = false;
	let lang = 'EN';

	function handleMenuState(event) {
		isMenuOpen = event.detail.isMenuOpen;
	}
</script>

<Navbar color="light" light expand="md" fixed="top">
	<NavbarBrand href="#home">
		<Logo height={50} />
	</NavbarBrand>
	<Button outline color="primary" href={APP_LINK} class="ml-auto d-md-none">Get free Pro</Button>
	<NavbarToggler on:click={() => (isMenuOpen = !isMenuOpen)} color="light" class="ml-2" />
	<Collapse isOpen={isMenuOpen} navbar expand="md" on:update={handleMenuState}>
		<Nav class="ml-auto text-center" navbar>
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
				<DropdownToggle nav caret class="d-flex justify-content-center align-items-center">
					<FlagIcon flag={lang} />
				</DropdownToggle>
				<DropdownMenu right>
					<DropdownItem active={lang === 'EN'} on:click={() => (lang = 'EN')}>
						<div class="d-flex align-items-center">
							<FlagIcon flag="EN" />
							<div class="ml-3">English</div>
						</div>
					</DropdownItem>
					<DropdownItem active={lang === 'RU'} on:click={() => (lang = 'RU')}>
						<div class="d-flex align-items-center">
							<FlagIcon flag="RU" />
							<div class="ml-3">Русский</div>
						</div>
					</DropdownItem>
				</DropdownMenu>
			</UncontrolledDropdown>
			<NavItem class="ml-2 d-none d-md-block">
				<Button outline color="primary" href={APP_LINK}>Get free Pro</Button>
			</NavItem>
		</Nav>
	</Collapse>
</Navbar>

<style lang="scss">
</style>
