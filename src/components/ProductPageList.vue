<template>
	<ul class="product-list">
		<ProductItem v-for="card in cards" :key="card.id" :card="card" />
	</ul>
</template>

<script>
import ProductItem from "./ProductPageListItem";
export default {
	components: {
		ProductItem,
	},

	data() {
		return {
			cards: [
				{
					id: 0,
					brand: "Бренд",
					title:
						"Полное название товара в несколько строк для вида с обрывом в конце Полное название товара в несколько строк для вида с обрывом в конце",
					price: 5990,
					specialPrice: 5990,
					isAvailable: true,
					isHit: true,
					isOffer: true,
					image: "item-image.svg",
				},
				{
					id: 2,
					brand: "Бренд",
					title:
						"Полное название товара в несколько строк для вида с обрывом в конце Полное название товара в несколько строк для вида с обрывом в конце",
					price: 5990,
					specialPrice: 5990,
					isAvailable: true,
					isHit: true,
					isOffer: true,
					image: "item-image.svg",
				},
				{
					id: 3,
					brand: "Бренд",
					title:
						"Полное название товара в несколько строк для вида с обрывом в конце Полное название товара в несколько строк для вида с обрывом в конце",
					price: 5990,
					specialPrice: 5990,
					isAvailable: false,
					isHit: true,
					isOffer: false,
					image: "item-image.svg",
				},
				{
					id: 4,
					brand: "Бренд",
					title:
						"Полное название товара в несколько строк для вида с обрывом в конце, Полное название товара в несколько строк для вида с обрывом в конце",
					price: 5990,
					specialPrice: 5990,
					isAvailable: true,
					isHit: false,
					isOffer: true,
					image: "item-image.svg",
				},
				{
					id: 5,
					brand: "Бренд",
					title:
						"Полное название товара в несколько строк для вида с обрывом в конце",
					price: 5990,
					specialPrice: 5990,
					isAvailable: true,
					isHit: true,
					isOffer: true,
					image: "item-image.svg",
				},
				{
					id: 6,
					brand: "Бренд",
					title:
						"Полное название товара в несколько строк для вида с обрывом в конце",
					price: 5990,
					specialPrice: 5990,
					isAvailable: true,
					isHit: true,
					isOffer: true,
					image: "item-image.svg",
				},
				{
					id: 7,
					brand: "Бренд",
					title:
						"Полное название товара в несколько строк для вида с обрывом в конце",
					price: 5990,
					specialPrice: 5990,
					isAvailable: true,
					isHit: true,
					isOffer: true,
					image: "item-image.svg",
				},
				{
					id: 8,
					brand: "Бренд",
					title:
						"Полное название товара в несколько строк для вида с обрывом в конце",
					price: 5990,
					specialPrice: 5990,
					isAvailable: true,
					isHit: true,
					isOffer: true,
					image: "item-image.svg",
				},
				{
					id: 9,
					brand: "Бренд",
					title:
						"Полное название товара в несколько строк для вида с обрывом в конце",
					price: 5990,
					specialPrice: 5990,
					isAvailable: true,
					isHit: false,
					isOffer: false,
					image: "item-image.svg",
				},
				{
					id: 10,
					brand: "Бренд",
					title:
						"Полное название товара в несколько строк для вида с обрывом в конце",
					price: 5990,
					specialPrice: 5990,
					isAvailable: true,
					isHit: false,
					isOffer: true,
					image: "item-image.svg",
				},
				{
					id: 11,
					brand: "Бренд",
					title:
						"Полное название товара в несколько строк для вида с обрывом в конце",
					price: 5990,
					specialPrice: 5990,
					isAvailable: true,
					isHit: true,
					isOffer: true,
					image: "item-image.svg",
				},
				{
					id: 12,
					brand: "Бренд",
					title:
						"Полное название товара в несколько строк для вида с обрывом в конце",
					price: 5990,
					specialPrice: 5990,
					isAvailable: true,
					isHit: true,
					isOffer: true,
					image: "item-image.svg",
				},
			],
		};
	},
};
</script>

<style lang="scss" scoped>
.product-list {
	display: grid;
	grid-template-columns: repeat(4, 1fr);
	gap: 24px;

	@media (max-width: 767px) {
		grid-template-columns: repeat(2, 1fr);
	}
}
</style>
