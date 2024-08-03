<template>
	<nav class="navigation">
		<a class="navigation__catalog">Каталог</a>
		<NavigationSearch class="navigation__search" />
		<NavigationList class="navigation__list" />
	</nav>
</template>

<script>
import NavigationList from "./HeaderNavigationList";
import NavigationSearch from "./HeaderNavigationSearch";
export default {
	components: {
		NavigationList,
		NavigationSearch,
	},
};
</script>

<style lang="scss" scoped>
.navigation {
	display: flex;
	align-items: center;
	gap: 24px;

	width: 100%;

	&__catalog {
		padding: 15.5px 24px;

		background-color: var(--white);
		border-radius: 8px;
		border: 1px solid #73aff4;

		font-family: "Inter", sans-serif;
		font-size: 14px;
		line-height: normal;
		font-weight: 500;

		cursor: pointer;
		transition: background-color 0.3s ease-in-out, color 0.3s ease-in-out;

		&:hover {
			background-color: var(--provence);
			color: var(--white);
		}
	}

	&__list,
	&__search {
		@media (max-width: 767px) {
			display: none;
		}
	}
}
</style>
