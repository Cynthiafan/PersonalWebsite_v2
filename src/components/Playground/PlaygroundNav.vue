<template>
  <v-navigation-drawer clipped fixed v-model="drawer" app>
    <v-list dense>
      <v-list-tile @click="">
        <v-list-tile-action>
          <v-icon>dashboard</v-icon>
        </v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-title>Dashboard</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
      <v-list-tile @click="">
        <v-list-tile-action>
          <v-icon>settings</v-icon>
        </v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-title>Settings</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>

      <v-list-group
    prepend-icon="account_circle"
    value="true"
  >
    <v-list-tile slot="activator">
      <v-list-tile-title>Users</v-list-tile-title>
    </v-list-tile>
    <v-list-group
      sub-group
      no-action
      value="true"
    >
      <v-list-tile slot="activator">
        <v-list-tile-title>Admin</v-list-tile-title>
      </v-list-tile>
      <v-list-tile
        v-for="(admin, i) in admins"
        :key="i"
        @click=""
      >
        <v-list-tile-title v-text="admin[0]"></v-list-tile-title>
        <v-list-tile-action>
          <v-icon v-text="admin[1]"></v-icon>
        </v-list-tile-action>
      </v-list-tile>
    </v-list-group>
    <v-list-group
      sub-group
      no-action
    >
      <v-list-tile slot="activator">
        <v-list-tile-title>Actions</v-list-tile-title>
      </v-list-tile>
      <v-list-tile
        v-for="(crud, i) in cruds"
        :key="i"
        @click=""
      >
        <v-list-tile-title v-text="crud[0]"></v-list-tile-title>
        <v-list-tile-action>
          <v-icon v-text="crud[1]"></v-icon>
        </v-list-tile-action>
      </v-list-tile>
    </v-list-group>
  </v-list-group>

    </v-list>
  </v-navigation-drawer>
</template>
