<template>
    <v-card class="mx-auto mt-5" max-width="500">
      <v-toolbar color="primary" dark>
        <v-card-title class="text-center">Mainframe</v-card-title>
      </v-toolbar>
  
      <v-card-text>
        <v-tabs v-model="activeTab">
          <v-tab v-for="tab in tabs" :key="tab.id">{{ tab.name }}</v-tab>
          <v-tab-item v-for="tab in tabs" :key="tab.id">{{ tab.content }}</v-tab-item>
        </v-tabs>
      </v-card-text>
  
      <v-card-actions class="justify-center">
        <v-btn color="primary">Bouton 1</v-btn>
        <v-btn color="secondary">Bouton 2</v-btn>
        <v-btn color="warning">Bouton 3</v-btn>
      </v-card-actions>
    </v-card>
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
  