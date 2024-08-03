<template>
	<section class="product-page">
		<div class="product-page__sidebar">
			<ProductFilters />
		</div>

		<div class="product-page__mobile">
			<div class="product-page__head">
				<button class="product-page__back">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						width="20"
						height="20"
						viewBox="0 0 20 20"
						fill="currentColor"
					>
						<path
							opacity="0.3"
							fill-rule="evenodd"
							clip-rule="evenodd"
							d="M0.283445 10.6843C-0.0944816 10.3064 -0.0944816 9.69363 0.283445 9.3157L9.3157 0.283445C9.69363 -0.0944804 10.3064 -0.0944804 10.6843 0.283445C11.0622 0.661371 11.0622 1.27411 10.6843 1.65204L3.30408 9.03226L19.0323 9.03226C19.5667 9.03226 20 9.46553 20 10C20 10.5345 19.5667 10.9677 19.0323 10.9677L3.30408 10.9677L10.6843 18.348C11.0622 18.7259 11.0622 19.3386 10.6843 19.7166C10.3064 20.0945 9.69363 20.0945 9.3157 19.7166L0.283445 10.6843Z"
						/>
					</svg>
				</button>
				<form class="product-page__search">
					<input type="search" class="product-page__input" />

					<input type="submit" class="product-page__button" value="Найти" />
				</form>
			</div>

			<p class="product-page__category">Название категории</p>
		</div>

		<div class="product-page__cards-container">
			<ProductList />
		</div>
	</section>
</template>

<script>
import ProductFilters from "./ProductPageFilters";
import ProductList from "./ProductPageList";
export default {
	components: {
		ProductFilters,
		ProductList,
	},
};
</script>

<style lang="scss" scoped>
.product-page {
	display: grid;
	grid-template-columns: 280px 1fr;
	gap: 36px;

	@media (max-width: 767px) {
		display: flex;
		flex-direction: column;
		gap: 12px;
		&__sidebar {
			display: none;
		}
	}

	&__mobile {
		display: none;
		@media (max-width: 767px) {
			display: flex;
			flex-direction: column;
			gap: 12px;
		}
	}

	&__head {
		display: flex;
		align-items: center;
		gap: 16px;
	}

	&__back {
		cursor: pointer;
		color: var(--light-dark);
		transition: color 0.3s ease-in-out;

		&:hover {
			color: #000;
		}
	}
	&__search {
		position: relative;
		width: 100%;
	}

	&__input {
		width: 100%;
		padding: 8px 91px 14px 0;

		border-bottom: 1px solid var(--color-border);
		transition: border-color 0.3s ease-in-out;

		&:focus {
			border-color: var(--provence);
		}
	}

	&__reset {
		position: absolute;
		top: 50%;
		right: 91px;
		transform: translateY(-50%);

		width: 20px;
		height: 20px;

		cursor: pointer;
		background-image: url("../assets/images/clear-field.svg");
		background-repeat: no-repeat;
		background-size: cover;
		transition: background-image 0.3s ease-in-out;
	}

	&__button {
		position: absolute;
		top: 0;
		right: 0;
		padding: 12px 16px;
		border-radius: 5px;
		background-color: var(--provence);

		font-size: 16px;
		line-height: 14px;
		color: var(--white);
		cursor: pointer;
	}

	&__category {
		color: var(--light-dark);
		font-size: 22px;
		line-height: 28px;
	}
}
</style>
