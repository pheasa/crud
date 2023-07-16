<template>
    <table class="table">
        <thead>
                <tr >
                    <th v-for="label in tbheader" v-bind:key="label">
                        {{ label }}
                    </th>
                </tr>
            </thead>
        <tbody>
            <tr v-for="row in data" v-bind:key="row">
                <td>{{ row.id }}</td>
                <td>{{ row.name }}</td>
                <td>{{ row.email }}</td>
                <th>
                    <button  type="button" v-for="(value, key) in action[0]" v-bind:key="key" v-bind:class="value + ' me-2'">{{ key }}</button>
                </th>
            </tr>
        </tbody>
    </table>
</template>

<script>
export default {
    name: 'DataTable',
    props:['tbheader','data','action']
}
</script>
