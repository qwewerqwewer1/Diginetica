<template>
	<li class="card">
		<div class="card__head">
			<span class="card__hit" :class="card.isHit ? 'show' : ''"
				>Хит продаж
			</span>
			<span class="card__discount" :class="card.isOffer ? 'show' : ''"
				>25%</span
			>
			<img :src="getImage" class="card__image" alt="product image" />
		</div>
		<div class="card__info">
			<p class="card__brand">{{ card.brand }}</p>
			<a href="" target="_blank"
				><h3 class="card__title">{{ card.title }}</h3></a
			>
		</div>
		<div v-if="card.isAvailable" class="card__prices">
			<span class="card__price-current">{{ card.specialPrice }} ₽</span>
			<span v-if="card.isOffer" class="card__price-old"
				>{{ card.price }} ₽</span
			>
		</div>

		<button v-if="card.isAvailable" class="card__button">Купить</button>

		<a v-else href="#" class="card__arrival">Сообщить о поступлении</a>
	</li>
</template>

<script>
export default {
	props: {
		card: Object,
	},
	computed: {
		getImage() {
			return require(`@/assets/images/item-card/${this.card.image}`);
		},
	},
};
</script>

<style lang="scss" scoped>
.card {
	display: flex;
	flex-direction: column;
	gap: 16px;

	@media (max-width: 767px) {
		border-radius: 4px 4px 0 0;
		overflow: hidden;
	}

	&__head {
		position: relative;
		min-height: 200px;
		background-color: #f8f8fa;
	}

	&__hit {
		display: none;
		position: absolute;
		top: 12px;
		left: 12px;
		padding: 8px 32px 8px 8px;

		font-size: 14px;
		line-height: 16px;
		color: var(--light-dark);

		background-color: var(--white);
		background-image: url("@/assets/images/item-card/hit.svg");
		background-repeat: no-repeat;
		background-position: center right 8px;
	}

	&__discount {
		display: none;
		position: absolute;
		left: 12px;
		bottom: 12px;
		padding: 6px 10px;

		color: var(--white);
		font-size: 14px;
		line-height: 14px;
		font-weight: 700;

		border-radius: 4px;
		background-color: var(--provence);
	}

	&__hit,
	&__discount {
		&.show {
			display: initial;
		}
	}

	&__info {
		flex-grow: 1;

		display: flex;
		flex-direction: column;
		gap: 8px;
	}

	&__brand {
		color: var(--light-gray);
		font-size: 14px;
		line-height: 16px;
	}

	&__title {
		color: var(--light-dark);
		font-size: 14px;
		line-height: 16px;

		overflow: hidden;
		display: -webkit-box;
		-webkit-line-clamp: 2; // Определяем количество строк перед достижением многоточия
		-webkit-box-orient: vertical;
		text-overflow: ellipsis;

		cursor: pointer;
		transition: color 0.3s ease-in-out;

		&:hover {
			color: #125bae;
		}

		@media (max-width: 1919px) {
			-webkit-line-clamp: 3;
		}
	}

	&__prices {
		display: flex;
		align-items: center;
		gap: 8px;
	}

	&__price-current {
		color: var(--light-dark);
		font-size: 16px;
		line-height: 14px;
		font-weight: 700;
	}

	&__price-old {
		color: var(--light-gray);
		font-size: 12px;
		line-height: 14px;
		text-decoration: line-through;
	}

	&__button {
		align-self: flex-start;

		position: relative;
		display: flex;
		justify-content: center;
		align-items: center;

		padding: 12px 16px;

		color: var(--provence);
		font-size: 14px;
		line-height: 14px;
		font-weight: 700;

		border-radius: 4px;
		border: 1px solid var(--provence);
		background-color: var(--white);
		cursor: pointer;

		transition: background-color 0.3s ease-in-out, color 0.3s ease-in-out,
			box-shadow 0.3s ease-in-out;

		&:hover {
			background-color: var(--provence);
			color: var(--white);
			box-shadow: 1px 1px 1px #125bae;
		}

		&:active {
			top: 1px;
		}
	}

	&__arrival {
		display: flex;
		justify-content: center;
		align-items: center;

		padding: 12px 16px;

		color: var(--light-gray);
		font-size: 14px;
		line-height: 14px;
		font-weight: 700;

		border-radius: 4px;
		border: 1px solid var(--light-gray);
		background-color: var(--white);

		transition: border-color 0.3s ease-in-out, color 0.3s ease-in-out;
		cursor: pointer;

		&:hover {
			color: var(--light-dark);
			border-color: var(--light-dark);
		}
	}
}
</style>
