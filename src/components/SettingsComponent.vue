<template>
    <v-container>
        <p class="text-h5 mb-3">Cadastrar Itens no Cardápio</p>
        <v-divider />
        
        <v-row class="mt-4">
            <v-col cols="4">
                <v-card elevation="4" subtitle="Informações do Item">
                    <v-card-text>
                        <v-text-field variant="outlined" density="compact" color="pink" label="Título do item"></v-text-field>
                        <v-textarea label="Descrição do item" density="compact" variant="outlined" color="pink"></v-textarea>
                        <v-row>
                            <v-col cols="6">
                                <v-select color="pink" density="compact" variant="outlined" v-model="grupo" label="Grupo" :items="['Selecionar grupo', 'Pizzas', 'Bebidas']"></v-select>
                            </v-col>
                            <v-col cols="6" v-if="grupo === 'Pizzas'">
                                <v-select v-model="subgrupo1" variant="outlined" density="compact" color="pink" label="Subgrupo" :items="['Doces', 'Salgadas']"></v-select>
                            </v-col>
                            <v-col cols="6" v-if="grupo === 'Bebidas'">
                                <v-select v-model="subgrupo2" variant="outlined" density="compact" color="pink" label="Subgrupo" :items="['Refrigerantes', 'Jarra de Suco', 'Cervejas', 'Águas']"></v-select>
                            </v-col>
                        </v-row>
                        <v-select v-if="grupo === 'Pizzas'" v-model="tamanho" color="pink" density="compact" variant="outlined" label="Tamanho" :items="['Grande', 'Média', 'Pequena']"></v-select>
                        <v-select v-if="grupo === 'Bebidas'" v-model="tamanho" color="pink" density="compact" variant="outlined" label="Quantidade" :items="['Grande', 'Média', 'Pequena']"></v-select>
                    </v-card-text>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
    export default {
        name: "SettingsComponent",
        data() {
            return {
                grupo: "Selecionar grupo",
                subgrupo1: "Doces",
                subgrupo2: "Refrigerantes",
                tamanho: 'Grande'
            }
        }
    }
</script>