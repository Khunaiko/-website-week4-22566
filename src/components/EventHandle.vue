<template>
    <div>
        <!-- <h1>Week3:Event Handling</h1>
        <hr />
        <p>{{ name }} {{ego}}</p>
        <button @:click="changName('Elon Musk'), changeEgo('starlord')">Change name</button> -->
        <p>Name:{{ name }}</p>
        <input type="text" @input="getInput($event, 'Tommy', 50)">
    </div>
</template>

<script>
export default {
    name: 'EventHandle',
    data() {
        return {
            name: "",
            ego:"Actor",
        }
    },
    methods: {
        changName(nameParams) {
            this.name = nameParams
        },
        changeEgo(egoParams) {
            this.ego = egoParams
        },
        getInput(event,lastname, age) {
            this.name = event.target.value + '' + lastname + '' + age
            console.log(event,lastname)
        }
    }
}
</script>