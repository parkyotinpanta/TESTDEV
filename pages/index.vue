<template>
    <div>
        
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
                  
                </tr>
            </thead>
            <tbody>
                <tr v-for="(item, index) in people" :key="item.ven_code_run" 
                @click=route(item)
                >
                    <td>{{ item.branch_no }}</td>
                    <td>{{ item.pre_name }}</td>
                    <td>{{ item.add_phone }}</td>
                    <td>{{ item.contact_name }}</td>
                    <td>{{ item.AF_Status }}</td>
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
const data = { "pre_name": "จ่าตุง" };


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
    router.push('/view/'+item.pre_name)
   

}

</script>