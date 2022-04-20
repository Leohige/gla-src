<template>
    <div class="bg-white max-w-1xl shadow overflow-hidden sm:rounded-lg">
        <div class="border-t border-gray-200">
            <dl>
                <div class="bg-gray-50 px-4 py-5 sm:grid sm:grid-cols-9 sm:gap-4 sm:px-6 flex items-center">
                    <dt class="text-sm font-medium text-gray-500 sm:col-span-1 text-center align-middle">
                        Ativo
                    </dt>
                    <dt class="text-sm font-medium text-gray-500 sm:col-span-2 text-center align-middle">
                        Item
                    </dt>
                    <dd class="text-sm font-medium text-gray-500 sm:col-span-2 text-center align-middle">
                        Nivel Atual
                    </dd>
                    <dd class="text-sm font-medium text-gray-500 sm:col-span-2 text-center align-middle">
                        Nivel Desejado
                    </dd>
                    <dd class="text-sm font-medium text-gray-500 sm:col-span-2 text-center align-middle">
                        Tentativas
                    </dd>
                </div>
                <div class="bg-white px-4 py-5 sm:grid sm:grid-cols-9 sm:gap-4 sm:px-6 text-center">
                    <dt class="text-sm font-medium text-gray-500 sm:col-span-1 text-center align-middle">
                        <input type="checkbox" class="accent-purple-500 h-6 w-6 border border-gray-300 rounded-md" v-model="head.active">
                    </dt>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        Cabeça
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 flex items-center max-w-md mx-auto w-28">
                        <input v-model="head.current_level" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2  flex items-center max-w-md mx-auto w-28">
                        <input v-model="head.desired_level" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2  flex items-center max-w-md mx-auto w-28">
                        <input v-model="head.tries" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                </div>

                <div class="bg-white px-4 py-5 sm:grid sm:grid-cols-9 sm:gap-4 sm:px-6 text-center">
                    <dt class="text-sm font-medium text-gray-500 sm:col-span-1 text-center align-middle">
                        <input type="checkbox" class="accent-purple-500 h-6 w-6 border border-gray-300 rounded-md" v-model="legs.active">
                    </dt>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        Calça
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 flex items-center max-w-md mx-auto w-28">
                        <input v-model="legs.current_level" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2  flex items-center max-w-md mx-auto w-28">
                        <input v-model="legs.desired_level" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2  flex items-center max-w-md mx-auto w-28">
                        <input v-model="legs.tries" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                </div>

                <div class="bg-white px-4 py-5 sm:grid sm:grid-cols-9 sm:gap-4 sm:px-6 text-center">
                    <dt class="text-sm font-medium text-gray-500 sm:col-span-1 text-center align-middle">
                        <input type="checkbox" class="accent-purple-500 h-6 w-6 border border-gray-300 rounded-md" v-model="emblem.active">
                    </dt>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        Emblema
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 flex items-center max-w-md mx-auto w-28">
                        <input v-model="emblem.current_level" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2  flex items-center max-w-md mx-auto w-28">
                        <input v-model="emblem.desired_level" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2  flex items-center max-w-md mx-auto w-28">
                        <input v-model="emblem.tries" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                </div>

                <div class="bg-white px-4 py-5 sm:grid sm:grid-cols-9 sm:gap-4 sm:px-6 text-center">
                    <dt class="text-sm font-medium text-gray-500 sm:col-span-1 text-center align-middle">
                        <input type="checkbox" class="accent-purple-500 h-6 w-6 border border-gray-300 rounded-md" v-model="body.active">
                    </dt>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        Corpo
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 flex items-center max-w-md mx-auto w-28">
                        <input v-model="body.current_level" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2  flex items-center max-w-md mx-auto w-28">
                        <input v-model="body.desired_level" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2  flex items-center max-w-md mx-auto w-28">
                        <input v-model="body.tries" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                </div>

                <div class="bg-white px-4 py-5 sm:grid sm:grid-cols-9 sm:gap-4 sm:px-6 text-center">
                    <dt class="text-sm font-medium text-gray-500 sm:col-span-1 text-center align-middle">
                        <input type="checkbox" class="accent-purple-500 h-6 w-6 border border-gray-300 rounded-md" v-model="weapon.active">
                    </dt>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        Arma
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 flex items-center max-w-md mx-auto w-28">
                        <input v-model="weapon.current_level" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2  flex items-center max-w-md mx-auto w-28">
                        <input v-model="weapon.desired_level" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2  flex items-center max-w-md mx-auto w-28">
                        <input v-model="weapon.tries" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                </div>

                <div class="bg-white px-4 py-5 sm:grid sm:grid-cols-9 sm:gap-4 sm:px-6 text-center">
                    <dt class="text-sm font-medium text-gray-500 sm:col-span-1 text-center align-middle">
                        <input type="checkbox" class="accent-purple-500 h-6 w-6 border border-gray-300 rounded-md" v-model="accessory.active">
                    </dt>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        Acessório
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 flex items-center max-w-md mx-auto w-28">
                        <input v-model="accessory.current_level" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2  flex items-center max-w-md mx-auto w-28">
                        <input v-model="accessory.desired_level" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2  flex items-center max-w-md mx-auto w-28">
                        <input v-model="accessory.tries" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                </div>
                
            </dl>
        </div>
    </div>

    <div class="bg-white max-w-1xl shadow overflow-hidden sm:rounded-lg mt-10">
        <div class="border-t border-gray-200">
            <dl>
                <div class="bg-gray-50 px-4 py-5 sm:grid sm:grid-cols-12 sm:gap-4 sm:px-6 flex items-center">
                    <dt class="text-sm font-medium text-gray-500 sm:col-span-2 text-center align-middle">
                        Pedra
                    </dt>
                    <dt class="text-sm font-medium text-gray-500 sm:col-span-2 text-center align-middle">
                        Mínimo
                    </dt>
                    <dd class="text-sm font-medium text-gray-500 sm:col-span-2 text-center align-middle">
                        Máximo
                    </dd>
                    <dd class="text-sm font-medium text-gray-500 sm:col-span-2 text-center align-middle">
                        Valor
                    </dd>
                    <dd class="text-sm font-medium text-gray-500 sm:col-span-2 text-center align-middle">
                        Total Mínimo
                    </dd>
                    <dd class="text-sm font-medium text-gray-500 sm:col-span-2 text-center align-middle">
                        Total Máximo
                    </dd>
                </div>
                <div class="bg-white px-4 py-5 sm:grid sm:grid-cols-12 sm:gap-4 sm:px-6 text-center">
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        Céu
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        {{ minSky }}
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        {{ maxSky }}
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 flex items-center max-w-md mx-auto w-28">
                        <input v-model="prices.sky" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        {{ minSkyPrice.toLocaleString('pt-BR') }}
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        {{ maxSkyPrice.toLocaleString('pt-BR') }}
                    </dd>
                </div>

                <div class="bg-white px-4 py-5 sm:grid sm:grid-cols-12 sm:gap-4 sm:px-6 text-center">
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        Sábio
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        {{ minWisdom }}
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        {{ maxWisdom }}
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 flex items-center max-w-md mx-auto w-28">
                        <input v-model="prices.wisdom" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        {{ minWisdomPrice.toLocaleString('pt-BR') }}
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        {{ maxWisdomPrice.toLocaleString('pt-BR') }}
                    </dd>
                </div>

                <div class="bg-white px-4 py-5 sm:grid sm:grid-cols-12 sm:gap-4 sm:px-6 text-center">
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        Carmesin
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        {{ minCarmesin }}
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        {{ maxCarmesin }}
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 flex items-center max-w-md mx-auto w-28">
                        <input v-model="prices.carmesin" type="text" id="create-account-first-name" class="text-center rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent" name="First name"/>
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        {{ minCarmesinPrice.toLocaleString('pt-BR') }}
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        {{ maxCarmesinPrice.toLocaleString('pt-BR') }}
                    </dd>
                </div>

                <div class="bg-white px-4 py-5 sm:grid sm:grid-cols-12 sm:gap-4 sm:px-6 text-center">
                    <dt class="text-sm font-medium text-gray-500 sm:col-span-2 text-center align-middle">
                        
                    </dt>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 flex items-center max-w-md mx-auto w-28">
                        
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 flex items-center max-w-md mx-auto w-28">
                        
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 flex items-center max-w-md mx-auto w-28">
                        
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        {{ minTotal.toLocaleString('pt-BR') }}
                    </dd>
                    <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2 text-center align-middle">
                        {{ maxTotal.toLocaleString('pt-BR') }}
                    </dd>
                </div>

            </dl>
        </div>
    </div>
</template>

<script>


export default {
    data() {
        return {
            head: {
                active: false,
                current_level: 0,
                desired_level: 0,
                tries: 0,
                stones: {
                    min: {
                        sky: 0,
                        wisdom: 0,
                        carmesin: 0
                    },
                    max: {
                        sky: 0,
                        wisdom: 0,
                        carmesin: 0
                    }
                }
            },
            body: {
                active: false,
                current_level: 0,
                desired_level: 0,
                tries: 0,
                stones: {
                    min: {
                        sky: 0,
                        wisdom: 0,
                        carmesin: 0
                    },
                    max: {
                        sky: 0,
                        wisdom: 0,
                        carmesin: 0
                    }
                }
            },
            legs: {
                active: false,
                current_level: 0,
                desired_level: 0,
                tries: 0,
                stones: {
                    min: {
                        sky: 0,
                        wisdom: 0,
                        carmesin: 0
                    },
                    max: {
                        sky: 0,
                        wisdom: 0,
                        carmesin: 0
                    }
                }
            },
            emblem: {
                active: false,
                current_level: 0,
                desired_level: 0,
                tries: 0,
                stones: {
                    min: {
                        sky: 0,
                        wisdom: 0,
                        carmesin: 0
                    },
                    max: {
                        sky: 0,
                        wisdom: 0,
                        carmesin: 0
                    }
                }
            },
            weapon: {
                active: false,
                current_level: 0,
                desired_level: 0,
                tries: 0,
                stones: {
                    min: {
                        sky: 0,
                        wisdom: 0,
                        carmesin: 0
                    },
                    max: {
                        sky: 0,
                        wisdom: 0,
                        carmesin: 0
                    }
                }
            },
            accessory: {
                active: false,
                current_level: 0,
                desired_level: 0,
                tries: 0,
                stones: {
                    min: {
                        sky: 0,
                        wisdom: 0,
                        carmesin: 0
                    },
                    max: {
                        sky: 0,
                        wisdom: 0,
                        carmesin: 0
                    }
                }
            },
            tries_per_level: {
                '1': 3,
                '2': 4,
                '3': 5,
                '4': 6,
                '5': 5,
                '6': 6,
                '7': 8,
                '8': 11,
                '9': 11,
                '10': 12,
                '11': 13,
                '12': 15,
            },
            stone_min_level: {
                'sky': 0,
                'wisdom': 5,
                'carmesin': 9
            },
            stone_max_level: {
                'sky': 4,
                'wisdom': 8,
                'carmesin': 12
            },
            prices: {
                sky: 0,
                wisdom: 0,
                carmesin: 0
            }
        }
    },
    computed: {
        minSky() {
            return this.head.stones.min.sky + this.legs.stones.min.sky + this.emblem.stones.min.sky + this.body.stones.min.sky + this.weapon.stones.min.sky + this.accessory.stones.min.sky;
        },
        minWisdom() {
            return this.head.stones.min.wisdom + this.legs.stones.min.wisdom + this.emblem.stones.min.wisdom + this.body.stones.min.wisdom + this.weapon.stones.min.wisdom + this.accessory.stones.min.wisdom;
        },
        minCarmesin() {
            return this.head.stones.min.carmesin + this.legs.stones.min.carmesin + this.emblem.stones.min.carmesin + this.body.stones.min.carmesin + this.weapon.stones.min.carmesin + this.accessory.stones.min.carmesin;
        },
        minSkyPrice() {
            return this.minSky * this.prices.sky;
        },
        minWisdomPrice() {
            return this.minWisdom * this.prices.wisdom;
        },
        minCarmesinPrice() {
            return this.minCarmesin * this.prices.carmesin;
        },
        minTotal() {
            return (this.minSkyPrice + this.minWisdomPrice + this.minCarmesinPrice);
        },

        maxSky() {
            return this.head.stones.max.sky + this.legs.stones.max.sky + this.emblem.stones.max.sky + this.body.stones.max.sky + this.weapon.stones.max.sky + this.accessory.stones.max.sky;
        },
        maxWisdom() {
            return this.head.stones.max.wisdom + this.legs.stones.max.wisdom + this.emblem.stones.max.wisdom + this.body.stones.max.wisdom + this.weapon.stones.max.wisdom + this.accessory.stones.max.wisdom;
        },
        maxCarmesin() {
            return this.head.stones.max.carmesin + this.legs.stones.max.carmesin + this.emblem.stones.max.carmesin + this.body.stones.max.carmesin + this.weapon.stones.max.carmesin + this.accessory.stones.max.carmesin;
        },
        maxSkyPrice() {
            return this.maxSky * this.prices.sky;
        },
        maxWisdomPrice() {
            return this.maxWisdom * this.prices.wisdom;
        },
        maxCarmesinPrice() {
            return this.maxCarmesin * this.prices.carmesin;
        },
        maxTotal() {
            return (this.maxSkyPrice + this.maxWisdomPrice + this.maxCarmesinPrice);
        }
    },
    methods: {
        reset: function() {
            this.head.stones.min.sky = 0;
            this.head.stones.min.wisdom = 0;
            this.head.stones.min.carmesin = 0;
            this.legs.stones.min.sky = 0;
            this.legs.stones.min.wisdom = 0;
            this.legs.stones.min.carmesin = 0;
            this.emblem.stones.min.sky = 0;
            this.emblem.stones.min.wisdom = 0;
            this.emblem.stones.min.carmesin = 0;
            this.body.stones.min.sky = 0;
            this.body.stones.min.wisdom = 0;
            this.body.stones.min.carmesin = 0;
            this.weapon.stones.min.sky = 0;
            this.weapon.stones.min.wisdom = 0;
            this.weapon.stones.min.carmesin = 0;
            this.accessory.stones.min.sky = 0;
            this.accessory.stones.min.wisdom = 0;
            this.accessory.stones.min.carmesin = 0;

            this.head.stones.max.sky = 0;
            this.head.stones.max.wisdom = 0;
            this.head.stones.max.carmesin = 0;
            this.legs.stones.max.sky = 0;
            this.legs.stones.max.wisdom = 0;
            this.legs.stones.max.carmesin = 0;
            this.emblem.stones.max.sky = 0;
            this.emblem.stones.max.wisdom = 0;
            this.emblem.stones.max.carmesin = 0;
            this.body.stones.max.sky = 0;
            this.body.stones.max.wisdom = 0;
            this.body.stones.max.carmesin = 0;
            this.weapon.stones.max.sky = 0;
            this.weapon.stones.max.wisdom = 0;
            this.weapon.stones.max.carmesin = 0;
            this.accessory.stones.max.sky = 0;
            this.accessory.stones.max.wisdom = 0;
            this.accessory.stones.max.carmesin = 0;
        },
        calcItemStones: function(type, stone, value) {
            let current_level = Number(type.current_level) + 1;
            let desired_level = Number(type.desired_level);
            let current_tries = Number(type.tries);
            type.stones.min[stone] = 0;
            type.stones.max[stone] = 0;

            if (desired_level < this.stone_min_level[stone]) {
                return;
            }

            if (current_level < this.stone_min_level[stone]) {
                current_level = this.stone_min_level[stone];
                current_tries = 0;
            }

            for (let i = current_level; i <= desired_level; i++) {
                if (i > this.stone_max_level[stone]) {
                    return;
                }

                type.stones.min[stone] += value;
                type.stones.max[stone] += value * (this.tries_per_level[i] - current_tries);
                current_tries = 0;

                if (type.stones.max[stone] < 0) {
                    type.stones.max[stone] = 0;
                }
            }
        },
        computeStone: function() {
            this.reset()

            if (this.head.active) {
                this.calcItemStones(this.head, 'sky', 2);
                this.calcItemStones(this.head, 'wisdom', 2);
                this.calcItemStones(this.head, 'carmesin', 2);
            }

            if (this.legs.active) {
                this.calcItemStones(this.legs, 'sky', 2);
                this.calcItemStones(this.legs, 'wisdom', 2);
                this.calcItemStones(this.legs, 'carmesin', 2);
            }

            if (this.emblem.active) {
                this.calcItemStones(this.emblem, 'sky', 2);
                this.calcItemStones(this.emblem, 'wisdom', 2);
                this.calcItemStones(this.emblem, 'carmesin', 2);
            }

            if (this.body.active) {
                this.calcItemStones(this.body, 'sky', 4);
                this.calcItemStones(this.body, 'wisdom', 4);
                this.calcItemStones(this.body, 'carmesin', 4);
            }

            if (this.weapon.active) {
                this.calcItemStones(this.weapon, 'sky', 4);
                this.calcItemStones(this.weapon, 'wisdom', 4);
                this.calcItemStones(this.weapon, 'carmesin', 4);
            }

            if (this.accessory.active) {
                this.calcItemStones(this.accessory, 'sky', 8);
                this.calcItemStones(this.accessory, 'wisdom', 8);
                this.calcItemStones(this.accessory, 'carmesin', 8);
            }
        }
    },
    watch: {
        'head.active'() { this.computeStone() },
        'head.current_level'() { this.computeStone() },
        'head.desired_level'() { this.computeStone() },
        'head.tries'() { this.computeStone() },
        'legs.active'() { this.computeStone() },
        'legs.current_level'() { this.computeStone() },
        'legs.desired_level'() { this.computeStone() },
        'legs.tries'() { this.computeStone() },
        'emblem.active'() { this.computeStone() },
        'emblem.current_level'() { this.computeStone() },
        'emblem.desired_level'() { this.computeStone() },
        'emblem.tries'() { this.computeStone() },
        'body.active'() { this.computeStone() },
        'body.current_level'() { this.computeStone() },
        'body.desired_level'() { this.computeStone() },
        'body.tries'() { this.computeStone() },
        'weapon.active'() { this.computeStone() },
        'weapon.current_level'() { this.computeStone() },
        'weapon.desired_level'() { this.computeStone() },
        'weapon.tries'() { this.computeStone() },
        'accessory.active'() { this.computeStone() },
        'accessory.current_level'() { this.computeStone() },
        'accessory.desired_level'() { this.computeStone() },
        'accessory.tries'() { this.computeStone() },        
    },
    setup() {
        
    },
}
</script>

