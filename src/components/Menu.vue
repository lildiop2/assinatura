<template>
    <v-list >
         <v-list-group
          sub-group
          no-action
        >
          <template v-slot:activator>
            <v-list-item-content>
              <v-list-item-title>CRUD SUBSCRIBER</v-list-item-title>
            </v-list-item-content>
          </template>

        <router-link to="/cadastrar">
          <v-list-item>
            <v-list-item-title > Cadastrar</v-list-item-title>
            <v-list-item-icon>
              <v-icon>mdi-plus-outline</v-icon>
            </v-list-item-icon>
          </v-list-item>
          </router-link>

            <router-link to="/pesquisar">
            <v-list-item>
            <v-list-item-title > Pesquisar</v-list-item-title>
            <v-list-item-icon>
              <v-icon>mdi-file-outline</v-icon>
            </v-list-item-icon>
          </v-list-item>
            </router-link>

            <router-link to="/atualizar">
            <v-list-item>
            <v-list-item-title > Atualizar</v-list-item-title>
            <v-list-item-icon>
              <v-icon>mdi-update</v-icon>
            </v-list-item-icon>
          </v-list-item>
            </router-link>

            <router-link to="/remover">
            <v-list-item>
            <v-list-item-title > Remover</v-list-item-title>
            <v-list-item-icon>
              <v-icon>mdi-delete</v-icon>
            </v-list-item-icon>
            </v-list-item>
            </router-link>

        </v-list-group>

         <v-list-group
          no-action
          sub-group
        >
          <template v-slot:activator>
            <v-list-item-content>
              <v-list-item-title>CRUD EMPRESA</v-list-item-title>
            </v-list-item-content>
          </template>

        <!-- <router-link to="/cadastrar">
          <v-list-item>
            <v-list-item-title > Cadastrar</v-list-item-title>
            <v-list-item-icon>
              <v-icon>mdi-plus-outline</v-icon>
            </v-list-item-icon>
          </v-list-item>
          </router-link> -->

            <!-- <router-link to="/pesquisar">
            <v-list-item>
            <v-list-item-title > Pesquisar</v-list-item-title>
            <v-list-item-icon>
              <v-icon>mdi-file-outline</v-icon>
            </v-list-item-icon>
          </v-list-item>
            </router-link>

            <router-link to="/atualizar">
            <v-list-item>
            <v-list-item-title > Atualizar</v-list-item-title>
            <v-list-item-icon>
              <v-icon>mdi-update</v-icon>
            </v-list-item-icon>
          </v-list-item>
            </router-link> -->

            <router-link to="/remover_empresa">
            <v-list-item>
            <v-list-item-title > Remover</v-list-item-title>
            <v-list-item-icon>
              <v-icon>mdi-delete</v-icon>
            </v-list-item-icon>
            </v-list-item>
            </router-link>

        </v-list-group>
    </v-list>
</template>

