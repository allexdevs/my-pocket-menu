<template>
    <v-container>
        <p class="text-h5 mb-3">Montar Pedido</p>
        <v-divider />
        <v-row class="mt-4">
            <v-col cols="2">
                <v-card subtitle="Opções do Cardápio" elevation="4">
                    <v-card-text class="px-0 pb-2">
                        <v-list lines="one">
                            <v-list-item rounded append-icon="mdi-chevron-right" prepend-icon="mdi-pizza" title="Pizzas"
                                value="1" />
                            <v-list-item rounded append-icon="mdi-chevron-right" prepend-icon="mdi-beer" title="Bebidas"
                                value="2" />
                        </v-list>
                    </v-card-text>
                </v-card>
            </v-col>
            <v-col cols="6">
                <v-card color="white" elevation="4" subtitle="Pesquisar Pizzas">
                    <v-card-text>
                        <v-text-field label="Digite o nome da pizza" clearable density="compact"
                            append-inner-icon="mdi-magnify" variant="outlined" rounded color="pink" />
                        <div class="d-flex flex-row align-center justify-end">
                            <v-pagination density="compact" v-model="page" :length="1" rounded="circle"></v-pagination>
                        </div>
                    </v-card-text>
                </v-card>

                <v-card elevation="4" class="mt-4" subtitle="Pizzas Disponíveis">
                    <v-card-text></v-card-text>
                </v-card>
            </v-col>
            <v-col cols="4">
                <v-card elevation="4" subtitle="Itens do Pedido"></v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    data() {
        return {
            page: 1
        }
    }
}
</script>