<template>
	<ul class="navigation-list">
		<li class="navigation-list__item" v-for="item in items" :key="item.id">
			<a :href="item.url" class="navigation-list__link" target="_blank">{{
				item.text
			}}</a>
		</li>
	</ul>
</template>

<script>
export default {
	data() {
		return {
			items: [
				{
					id: 1,
					url: "#",
					text: "Информация о компании",
				},
				{
					id: 2,
					url: "#",
					text: "Контакты",
				},
				{
					id: 3,
					url: "#",
					text: "Полезные ссылки",
				},
			],
		};
	},
};
</script>

<style lang="scss" scoped>
.navigation-list {
	display: flex;
	align-items: center;
	gap: 24px;

	&__link {
		padding: 10px 0;
		font-family: "Inter", sans-serif;
		font-size: 14px;
		line-height: normal;
		color: #393939;
		transition: color 0.3s ease-in-out;

		&:hover {
			color: var(--provence);
		}
	}
}
</style>
