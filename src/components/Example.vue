<template>
    <div class="py-4">
        <pre class="">{{query.trim()}}</pre>
        <button v-on:click="setGuess(query.trim())" class="bg-blue-800 text-blue-100 hover:bg-blue-500  hover:text-blue-100 mb-2 font-bold py-1 px-3 rounded text-left text-sm mt-2">
            Run example
        </button>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import { Query } from '@/database';

@Component
export default class Example extends Vue {
    @Prop() private query!: string;
    @Prop() private setGuess!: any;
}
</script>


