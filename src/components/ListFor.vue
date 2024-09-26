<template>
    <div>
        <ul>
            <li v-for="(list, index) in lists" :key="index">
                <h3>{{ list.title }}</h3>
                <p>{{ list.disc }}</p>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    data () {
        return {
            lists: [
                {
                    id: 1,
                    title: 'List item 1',
                    disc: 'discription list item 1'
                 },
                 {
                    id: 2,
                    title: 'List item 2',
                    disc: 'discription list item 2'
                 },
                 {
                    id: 3,
                    title: 'List item 3',
                    disc: 'discription list item 3'
                 },

            ]
        }
    },
    setup () {
        

        return {}
    }
}
</script>

<style lang="scss" scoped>
ul {
    list-style-type: none;
}

li {
    text-align: left;
}
</style>