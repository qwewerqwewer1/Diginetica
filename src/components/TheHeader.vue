<template>
	<header class="header">
		<a href="#" class="header__logo"
			><img
				src="../assets/images/header/logo.svg"
				alt="company`s logo"
				width="24"
				height="24"
			/>
			Логотип
		</a>
		<HeaderNavigation class="header__navigation" />
	</header>
</template>

<script>
import HeaderNavigation from "./HeaderNavigation";
export default {
	components: {
		HeaderNavigation,
	},
};
</script>

<style lang="scss" scoped>
.header {
	display: flex;
	align-items: center;
	gap: 8px;

	padding: 12px 0;
	margin-bottom: 24px;

	@media (max-width: 767px) {
		margin-bottom: 12px;
		justify-content: space-between;
	}

	&__logo {
		display: flex;
		align-items: center;
		gap: 8px;
		padding: 14.5px 24px;

		font-family: "Inter", sans-serif;
		font-size: 16px;
		line-height: normal;

		cursor: pointer;
	}

	&__navigation {
		@media (max-width: 767px) {
			width: auto;
		}
	}
}
</style>
