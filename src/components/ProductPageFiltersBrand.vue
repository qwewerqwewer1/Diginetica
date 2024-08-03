<template>
	<div class="brand">
		<div class="brand__head">
			<h2 class="brand__title">Бренд</h2>
			<button class="brand__reset">Очистить</button>
		</div>

		<form class="brand__form">
			<input type="search" class="brand__search" />
		</form>

		<FiltersList :brandList="brandList" />
	</div>
</template>

<script>
import FiltersList from "./ProductPageFiltersBrandList";

export default {
	components: {
		FiltersList,
	},

	data() {
		return {
			brandList: [
				{
					name: "brands",
					id: 0,
					name: "Атрибут",
					quantity: 3,
					value: "EA",
				},
				{
					name: "brands",
					id: 1,
					name: "Атрибут",
					quantity: 3,
					value: "EL",
				},
				{
					name: "brands",
					id: 2,
					name: "Атрибут",
					quantity: 3,
					value: "DG",
				},
				{
					name: "brands",
					id: 3,
					name: "Атрибут",
					quantity: 3,
					value: "CL",
				},
				{
					name: "brands",
					id: 4,
					name: "Атрибут",
					quantity: 3,
					value: "TH",
				},
				{
					name: "brands",
					id: 5,
					name: "Атрибут",
					quantity: 3,
					value: "ZL",
				},
				{
					name: "brands",
					id: 6,
					name: "Атрибут",
					quantity: 3,
					value: "CCJ",
				},
				{
					name: "brands",
					id: 7,
					name: "Атрибут",
					quantity: 3,
					value: "CSS",
				},
				{
					name: "brands",
					id: 8,
					name: "Атрибут",
					quantity: 3,
					value: "VUE",
				},
				{
					name: "brands",
					id: 9,
					name: "Атрибут",
					quantity: 3,
					value: "HTML",
				},
				{
					name: "brands",
					id: 10,
					name: "Атрибут",
					quantity: 3,
					value: "JS",
				},
				{
					name: "brands",
					id: 11,
					name: "Атрибут",
					quantity: 3,
					value: "MSI",
				},
			],
		};
	},
};
</script>

<style lang="scss" scoped>
.brand {
	display: flex;
	flex-direction: column;
	gap: 16px;

	&__head {
		display: flex;
		justify-content: space-between;
	}

	&__title {
		color: var(--light-dark);
		font-size: 16px;
		line-height: 20px;
		font-weight: 700;
	}

	&__reset {
		color: var(--light-gray);
		font-size: 12px;
		line-height: 12px;
		text-decoration: underline;
		cursor: pointer;

		transition: color 0.3s ease-in-out;

		&:hover {
			color: var(--light-dark);
		}
	}

	&__form {
		position: relative;

		&::before {
			content: "";
			position: absolute;
			top: 50%;
			left: 12px;
			transform: translateY(-50%);

			width: 16px;
			height: 16px;

			background-image: url("../assets/images/filters/sidebar-search.svg");
			background-repeat: no-repeat;
		}
	}

	&__search {
		width: 100%;
		padding: 10px 12px 10px 36px;
		border-radius: 4px;
		border: 1px solid var(--color-border);
		transition: border-color 0.3s ease-in-out;

		&:focus {
			border-color: var(--provence);
		}
	}
}
</style>
