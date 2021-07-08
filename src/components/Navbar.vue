<template>
  <nav>
    <v-app-bar
      color="#334257"
      dense
      elevate-on-scroll
      fixed
    >
      <v-app-bar-nav-icon class="grey--text" @click.stop="drawer=!drawer"></v-app-bar-nav-icon>
      <router-link class="ml-5" to="/" style="text-decoration:none">
        <v-app-bar-title class="text-uppercase white--text">
          <span class="font-weight-light">
            Final
          </span>
          <span>
            Project
          </span>
        </v-app-bar-title>
      </router-link>
      <v-spacer/>
      <v-btn color="#548CA8" to="/login" class="white--text">
        <span>Sign in</span>
        <v-icon>mdi-login</v-icon>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer"  color="#EEEEEE" app temporary>
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="text-h6">
            Post Training
          </v-list-item-title>
          <v-list-item-subtitle>
            by Kelompok 1
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>
      <v-list
        dense
        nav
      >
        <v-list-item
          link to="/addStudent"
        >
          <v-list-item-icon>
            <v-icon>mdi-account-plus</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>Add Student</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item
          link to="/addCourse"
        >
          <v-list-item-icon>
            <v-icon>mdi-book-plus</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>Add Course</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item
          link to="/enrollment"
        >
          <v-list-item-icon>
            <v-icon>mdi-view-dashboard</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>Enroll Course</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

  </nav>  
</template>

<script>
export default {
    data: () => ({
      drawer:false
    }),
}
</script>