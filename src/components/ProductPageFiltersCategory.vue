<template>
	<div class="category">
		<ul class="category__list">
			<li class="category__item" v-for="item in listItems" :key="item.id">
				<a class="category__link">
					{{ item.category }}
					<span class="quantity">{{ item.quantity }}</span>
				</a>

				<ul class="category__inner-list">
					<li
						class="category__inner-item"
						v-for="item in innerList"
						:key="item.id"
					>
						<a
							class="category__inner-link"
							:class="item.isActive ? 'active' : ''"
							>{{ item.category }}

							<span class="quantity">{{ item.quantity }}</span>
						</a>
					</li>
				</ul>
			</li>
		</ul>
	</div>
</template>

<script>
export default {
	data() {
		return {
			listItems: [
				{
					id: 0,
					category: "Название категории",
					quantity: 3,
					isActive: true,
				},
			],

			innerList: [
				{
					id: 0,
					category: "Название категории",
					quantity: 3,
					isActive: false,
				},
				{
					id: 1,
					category: "Название категории",
					quantity: 3,
					isActive: false,
				},
				{
					id: 2,
					category: "Название категории",
					quantity: 3,
					isActive: true,
				},
			],
		};
	},
};
</script>

<style lang="scss" scoped>
.category {
	&__list {
		display: flex;
		flex-direction: column;
	}

	&__item {
		display: flex;
		flex-direction: column;
	}

	&__link {
		display: flex;
		justify-content: space-between;
		padding: 7px 16px 7px 8px;
	}

	&__inner-link {
		display: flex;
		justify-content: space-between;
		padding: 7px 16px 7px 32px;

		&.active {
			background-color: var(--color-font-bg);

			.quantity {
				color: var(--light-dark);
			}
		}
	}

	&__link,
	&__inner-link {
		font-size: 14px;
		line-height: 16px;
		color: var(--light-dark);
		border-radius: 5px;
		transition: background-color 0.3s ease-in-out;

		cursor: pointer;

		&:hover:not(.active) {
			color: var(--provence);
			.quantity {
				color: var(--light-dark);
			}
		}
	}
}
</style>
