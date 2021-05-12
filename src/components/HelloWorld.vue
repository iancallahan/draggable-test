<template>
    <draggable v-model="disciplines" item-key="id">
         <template #item="{element}">
                <div class="w-full p-4 bg-gray-400 my-2 flex justify-center"><span>{{element.name}}</span></div>
         </template>
    </draggable>
</template>

<script>
import draggable from 'vuedraggable'
    export default {
        name: "Discipline Organizer",
        components: {draggable},
        data(){
            return {
                disciplines: [
                    {   name: "Morning Prayer",
                        id: 1,
                        position: 0,
                    },
                    {   name: "Angelus",
                        id: 2,
                        position: 1,
                    },
                    {   name: "Evening Prayer",
                        id: 3,
                        position: 2,
                    },
                    {   name: "Custom Activity",
                        id: 24,
                        position: 3,
                    },
                ]
            }
        }
    }
</script>