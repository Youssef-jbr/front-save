<template>
    <div>
        <v-card class="mx-auto mt-5" max-width="500">
      <v-toolbar color="secondary" dark>
        <v-card-title class="text-center">Mainframe</v-card-title>
      </v-toolbar>
  
      
  
      <v-card-text>
        <v-tabs v-model="activeTab">
          <v-tab v-for="tab in tabs" :key="tab.id">{{ tab.name }}</v-tab>
          <v-tab-item v-for="tab in tabs" :key="tab.id">{{ tab.content }}</v-tab-item>
        </v-tabs>
      </v-card-text>
  
      <v-card-actions class="justify-center">
            <v-btn class="secondary">
                <v-icon>mdi-download</v-icon>
                [TITLE]
            </v-btn>
            <v-btn class="secondary">
                <v-icon>mdi-download</v-icon>
                [TITLE]
            </v-btn>
            <v-btn class="secondary">
                <v-icon>mdi-download</v-icon>
                [TITLE]
            </v-btn>
      </v-card-actions>
    </v-card>

    <v-card class="mx-auto mt-5" max-width="500">
      <v-toolbar color="secondary" dark>
        <v-card-title class="text-center">Open</v-card-title>
      </v-toolbar>
  
      <v-card-title class="justify-center text-center">Télécharger les 3 derniers mois de sauvegarde</v-card-title>
  
      <v-card-actions class="justify-center">
            <v-btn class="secondary">
                <v-icon>mdi-download</v-icon>
                [TITLE]
            </v-btn>
            <v-btn class="secondary">
                <v-icon>mdi-download</v-icon>
                [TITLE]
            </v-btn>
            <v-btn class="secondary">
                <v-icon>mdi-download</v-icon>
                [TITLE]
            </v-btn>
      </v-card-actions>
      <v-divider></v-divider>

      <v-card-title class="justify-center text-center">Télécharger le fichier de sauvegarde ce mois</v-card-title>


        <v-card-actions class="justify-center">
            <v-btn class="error"><v-icon>mdi-download</v-icon>Mois courant</v-btn>
            <v-btn class="error">Mois courant -SIIS</v-btn>
        </v-card-actions>
        <v-card-actions class="justify-center">
            <v-btn class="secondary"><v-icon>mdi-download</v-icon>Nombre de serveurs orphelins :[___]</v-btn>
        </v-card-actions>
       </v-card>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        activeTab: 'tab1',
        tabs: [
          { id: 1, name: 'ILSI', content: 'Télécharger les 3 derniers mois de sauvegarde' },
          { id: 2, name: 'BATCH SAUVEGARDE', content: 'Télécharger le fichier batch sauvegarde ce mois' }
        ]
      }
    }
  }
  </script>
  