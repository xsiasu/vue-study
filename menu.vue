<template>
  <div class="text-center">
    <v-menu offset-y bottom>
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="primary"
          dark
          v-bind="attrs"
          v-on="on"
        >
          Dropdown
        </v-btn>
      </template>
      <v-list
       v-for="(item, index) in items"
          :key="index">
        <v-list-item
         v-if
         :key="index"
         :to="item.to"
         href
        >
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
        <v-divider
        v-else
        :key="item.title"
        >
      </v-list>
    </v-menu>
  </div>
</template>

<script>
  export default {
    data: () => ({
      items: [
        { title: 'Click Me' },
        { title: 'Click Me' },
        { title: 'Click Me' },
        { divider : false },
        { title: 'Click Me 2' },
      ],
    }),
  }
</script>
