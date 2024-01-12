<script setup>
import { defineEmits } from 'vue';

const Emits = defineEmits(['selectOption'])
const selectOption = (isColor) => {
    Emits("selectOption", isColor)
}
</script>

<template>
   <v-navigation-drawer
     expand-on-hover
     rail
   >
    <v-list>
        <v-list-item
        prepend-avatar="https://res.cloudinary.com/dqrykh6qy/image/upload/v1676592415/samples/backgrounds/48311435-5371-4784-AF61-048556EB7A40_xjksk5.jpg"
        title="Justice Odoyi"
        subtitle="justiceodoyi@gmail.com"
        ></v-list-item>
    </v-list>

    <v-divider />

    <v-list density="compact" nav>
        <v-list-item
            prepend-icon="mdi-image"
            title="Color Gallery"
            value="color"
            @click="selectOption(true)"
        />
        <v-list-item
            prepend-icon="mdi-dialpad"
            title="Grayspace Gallery"
            value="color"
            @click="selectOption(false)"
        />
    </v-list>
   </v-navigation-drawer>
</template>