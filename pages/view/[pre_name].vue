<template>
    <div>
        <v-text-field v-if="vendor" v-model="vendor.pre_name" label="ข้อมูลผู้จำหน่าย"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ven_code" label="เลขประจำตัวผู้เสียภาษี"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ven_name" label="สถานประกอบการ"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.contact_name" label="ชื่อผู้ติดต่อ"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_name" label="สถานที่ตั้ง"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_no" label="เลขที่"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_moo" label="หมู่"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_soi" label="ตรอก"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_trog" label="ซอย"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_road" label="ถนน"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_tumbol" label="แขวง/ตำบล"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_amphur" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_provid" label="จังหวัด"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_province" label="ภาค"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_zip" label="รหัสไปรษณีย์"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_tel" label="ติดต่อ"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_fax_ext" label="แฟกซ์"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_email" label="อีเมล"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.vengroup_code" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.vat_type" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.vat_code" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ven_discount" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ven_ship_term" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ven_ct_code" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ven_credit_term" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ven_balance" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.contact_fdate" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.contact_ldate" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.cancel_date" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.rec_memo" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ordering_date" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ordering_cycle" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.AF_Status" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ven_balance_cs" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.tax_id" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.tax_branch_id" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.tax_branch" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.dealercode" label="รหัสตัวแทนจำหน่าย"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_date" label="วันที่"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_time" label="เวลา"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.edit_date" label="วันที่"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.edit_time" label="เวลา"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_tel1_ext" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.vender_type" label="พิม"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_phone" label="เบอร์โทรศัพท์"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.sap_no" label="หมายเหตุ"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ven_credit_limit" label="เบอร์โทรศัพท์"></v-text-field>
        <h1 v-if="vendor">{{ vendor}}</h1>
    </div>
</template>
<script setup>
import axios from 'axios';
import { useRoute } from 'nuxt/app'
import { onMounted } from 'vue'


const route = useRoute()
const pre_name = route.params.pre_name
console.log(pre_name);
let vendor = ref()

onMounted(() => {
    axios.post('http://localhost:3050/api/where', { "pre_name": pre_name })
    .then((item) => {
        vendor.value = item.data
        console.log(item.data);
    })
    

})

</script>