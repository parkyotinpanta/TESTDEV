<template>
    <div>
        <v-btn color="green-darken-3" @click="insert('สร้างข้อมูลผู้จำหน่าย')">เพิ่มข้อมูลผู้จำหน่าย</v-btn>
        <v-text-field v-model="search"  label="ค้นหาข้อมูล"></v-text-field>
        <v-btn @click="searchVendor(search)" >  ค้นหา</v-btn>
        <v-btn @click="clear()" >  เคลียร์</v-btn>
        <v-table>
            <thead>
                <tr>
                    <th class="text-left">
                        รหัสผู้จำหน่าย
                    </th>
                    <th class="text-left">
                        ชื่อผู้จำหน่าย
                    </th>
                    <th class="text-left">
                        โทรศัพ
                    </th>
                    <th class="text-left">
                        ติดต่อ
                    </th>
                    <th class="text-left">
                        สถานะ
                    </th>
                    <th class="text-left">
                        ดู
                    </th>
                    <th class="text-left">
                        ลบ
                    </th>

                </tr>
            </thead>
            <tbody>
                <tr v-for="(item, index) in people" :key="item.ven_code_run">
                    <td>{{ item.branch_no }}</td>
                    <td>{{ item.pre_name }}</td>
                    <td>{{ item.add_phone }}</td>
                    <td>{{ item.contact_name }}</td>
                    <td>{{ item.AF_Status }}</td>
                    <td><v-btn class="ma-2" color="light-blue-darken-3" icon="mdi-eye-arrow-right" @click=route(item)></v-btn></td>
                    <td><v-btn class="ma-2" color="red-accent-4" icon="mdi-delete" @click="del(item.ven_code_run)"></v-btn>
                    </td>

                </tr>
            </tbody>
        </v-table>
    </div>
</template>

<script setup>
import { useRouter } from 'nuxt/app';
import axios from 'axios';
import { ref } from 'vue';
const people = ref({})
// const data = { "pre_name": "จ่าตุง" };
const search = ref()
function searchVendor(item) {
    console.log(!item)
    if (!item) {
        axios.get('http://localhost:3050/api/selete', { responseType: 'json', "Content-type": "application/x-www-form-urlencoded" })
                .then((data) => {
                    people.value = data.data
                })
                
    }else{
        axios.post('http://localhost:3050/api/search',{"search":item})
        .then((data)=>{
            people.value = data.data
        })
    }
}

const columns = [{

    key: 'branch_no',
    label: 'ลำดับ'
}, {
    key: 'branch_no',
    label: 'รหัสผู้จำหน่าย'
}, {
    key: 'pre_name',
    label: 'ชื่อผู้จำหน่าย'
}, {
    key: 'add_phone',
    label: 'เบอร์โทรศัพท์'
}, {
    key: 'contact_name',
    label: 'ติดต่อ'
}, {
    key: 'AF_Status',
    label: 'สถานะ'

}]
axios.get('http://localhost:3050/api/selete', { responseType: 'json', "Content-type": "application/x-www-form-urlencoded" }).then((item) => {
    people.value = item.data
})


function route(item) {
    // console.log(item);
    const router = useRouter()
    router.push('/view/' + item.pre_name)


}
function insert() {
    const router = useRouter()
    router.push('/insert/')
}
function del(item) {
    axios.post('http://localhost:3050/api/remove', { "ven_code_run": item })
        .then(() => {
            axios.get('http://localhost:3050/api/selete', { responseType: 'json', "Content-type": "application/x-www-form-urlencoded" })
                .then((item) => {
                    people.value = item.data
                })
        }) 
}


function clear() {
    search.value = null
    axios.get('http://localhost:3050/api/selete', { responseType: 'json', "Content-type": "application/x-www-form-urlencoded" })
                .then((data) => {
                    people.value = data.data
                })
}
</script>