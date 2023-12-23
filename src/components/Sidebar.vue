<template>
    <VNavigationDrawer
    expand-on-hover
    rail
    >
    <VList>
          <VListItem
            prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"
            title="Jael Kalvin"
            subtitle="jaelngaleu@gmailcom"
          ></VListItem>
        </VList>

        <v-divider></v-divider>

        <VList density="compact" nav>
          <VListItem prepend-icon="mdi-image" title="Color Gallery" value="color"></VListItem>
          <VListItem prepend-icon="mdi-dialpad" title="Grey Gallery" value="grey"></VListItem>
        </VList>
    </VNavigationDrawer>
</template>


