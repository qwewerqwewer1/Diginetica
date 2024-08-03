<template>
	<form class="navigation-search">
		<input
			type="search"
			class="navigation-search__input"
			placeholder="Поиск по 100 000 товаров "
		/>

		<button class="navigation-search__button" type="submit">
			<img src="../assets/images/header/search.svg" />
		</button>
	</form>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.navigation-search {
	flex: 1;
	position: relative;
	padding: 12px 16px 12px 48px;

	border-radius: 10px;
	border: 1px solid #73aff4;

	background: #fff;

	&__button {
		position: absolute;
		top: 50%;
		left: 16px;
		transform: translateY(-50%);

		height: 24px;
		cursor: pointer;
	}

	&__input {
		width: 100%;

		font-family: "Inter", sans-serif;
		font-size: 16px;
		line-height: 150%;
		color: #5a5a5a;
	}
}
</style>
