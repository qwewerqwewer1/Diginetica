<template>
	<div class="size">
		<h2 class="size__title">Размер</h2>
		<ProductSizeList :sizeList="sizeList" />
	</div>
</template>

<script>
import ProductSizeList from "./ProductPageFiltersSizeList";
export default {
	components: {
		ProductSizeList,
	},
	data() {
		return {
			sizeList: [
				{
					name: "sizes",
					id: 0,
					name: "Атрибут",
					quantity: 3,
					value: "xxs",
				},
				{
					name: "sizes",
					id: 1,
					name: "Атрибут",
					quantity: 3,
					value: "xs",
				},
				{
					name: "sizes",
					id: 2,
					name: "Атрибут",
					quantity: 3,
					value: "s",
				},
				{
					name: "sizes",
					id: 3,
					name: "Атрибут",
					quantity: 3,
					value: "m",
				},
				{
					name: "sizes",
					id: 4,
					name: "Атрибут",
					quantity: 3,
					value: "l",
				},
				{
					name: "sizes",
					id: 5,
					name: "Атрибут",
					quantity: 3,
					value: "xl",
				},
				{
					name: "sizes",
					id: 6,
					name: "Атрибут",
					quantity: 3,
					value: "xxl",
				},
				{
					name: "sizes",
					id: 7,
					name: "Атрибут",
					quantity: 3,
					value: "xxxl",
				},
				{
					name: "sizes",
					id: 8,
					name: "Атрибут",
					quantity: 3,
					value: "11",
				},
				{
					name: "sizes",
					id: 9,
					name: "Атрибут",
					quantity: 3,
					value: "10",
				},
				{
					name: "sizes",
					id: 10,
					name: "Атрибут",
					quantity: 3,
					value: "9",
				},
				{
					name: "sizes",
					id: 11,
					name: "Атрибут",
					quantity: 3,
					value: "13",
				},
			],
		};
	},
};
</script>

<style lang="scss" scoped>
.size {
	&__title {
		text-align: center;
		color: var(--light-dark);
		font-size: 16px;
		line-height: 20px;
		font-weight: 700;
	}
}
</style>
