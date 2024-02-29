<template>
    <div>
        <v-text-field v-if="vendor" v-model="vendor.pre_name" label="ข้อมูลผู้จำหน่าย"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.branch_no" label="เลขสาขา"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ven_code" label="เลขประจำตัวผู้เสียภาษี"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ven_name" label="นามสกุล"></v-text-field>
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
        <v-text-field v-if="vendor" v-model="vendor.vengroup_code" label="ประเภทการสั่งซื้อ"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.vat_type" label="ประเภทภาษี"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.vat_code" label="จำนวน"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ven_discount" label="การลดราคา"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ven_ship_term" label="ระยะเวลาจัดส่ง"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ven_ct_code" label="เลขของพัสถุ"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ven_credit_term" label="เครดิต"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ven_balance" label="งบ"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.contact_fdate" label="ติดต่อล่าสุด"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.contact_ldate" label="วันยกเลิกที่ติดต่อ"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.cancel_date" label="ยกเลิกข้อมูล"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.rec_memo" label="บันทึกช่วยจำ"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ordering_date" label="ข้อมูล"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ordering_cycle" label="รอบสั่งซื้อ"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.AF_Status" label="สถานะ"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ven_balance_cs" label="ภาษี"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.tax_id" label="ที่อยู่ของผู้จำหน่าย"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.tax_branch_id" label="ไอดีผู้จำหน่าย"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.tax_branch" label="ข้อมูลผู้จำหน่าย"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.dealercode" label="รหัสตัวแทนจำหน่าย"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_date" label="วันที่"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_time" label="เวลา"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.edit_date" label="วันที่"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.edit_time" label="เวลา"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_tel1_ext" label="วันที่ยกเลิก"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.vender_type" label="พิม"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.add_phone" label="เบอร์โทรศัพท์"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.sap_no" label="หมายเหตุ"></v-text-field>
        <v-text-field v-if="vendor" v-model="vendor.ven_credit_limit" label="เครดิต"></v-text-field>
        <v-btn color="grey-darken-4" @click="BLACK">BLACK</v-btn>
        <v-btn  color="green-darken-4" @click="UPDETE(vendor)">UPDETE </v-btn>

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
function BLACK() {
    const router = useRouter()
    router.push('/')
}
function UPDETE(item) {

    let { ven_code, ven_code_run, pre_name, ven_name, contact_name, add_name, add_no, add_moo, add_soi, add_trog
        , add_road, add_tumbol, add_amphur, add_provid, add_province, add_zip, add_tel, add_email, vengroup_code, vat_type
        , vat_code, ven_discount, ven_ship_term, ven_ct_code, ven_credit_term, ven_credit_limit, ven_balance, contact_fdate
        , contact_ldate, cancel_date, rec_memo, ordering_date, ordering_cycle, AF_Status, ven_balance_cs, tax_id, tax_branch_id
        , tax_branch, dealercode, add_date, add_time, edit_date, edit_time, add_tel1_ext, add_fax_ext, vender_type, add_phone, sap_no } = item
    let updataData = {
        "ven_code": ven_code,
        "ven_code_run": ven_code_run,
        "pre_name": pre_name,
        "ven_name": ven_name,
        "contact_name": contact_name,
        "add_name": add_name,
        "add_no": add_no,
        "add_moo": add_moo,
        "add_soi": add_soi,
        "add_trog": add_trog,
        "add_road": add_road,
        "add_tumbol": add_tumbol,
        "add_amphur": add_amphur,
        "add_provid": add_provid,
        "add_province": add_province,
        "add_zip": add_zip,
        "add_tel": add_tel,
        "add_email": add_email,
        "vengroup_code": vengroup_code,
        "vat_type": vat_type,
        "vat_code": vat_code,
        "ven_discount": ven_discount,
        "ven_ship_term": ven_ship_term,
        "ven_ct_code": ven_ct_code,
        "ven_credit_term": ven_credit_term,
        "ven_credit_limit": ven_credit_limit,
        "ven_balance": ven_balance,
        "contact_fdate": contact_fdate,
        "contact_ldate": contact_ldate,
        "cancel_date": cancel_date,
        "rec_memo": rec_memo,
        "ordering_date": ordering_date,
        "ordering_cycle": ordering_cycle,
        "AF_Status": AF_Status,
        "ven_balance_cs": ven_balance_cs,
        "tax_id": tax_id,
        "tax_branch_id": tax_branch_id,
        "tax_branch": tax_branch,
        "dealercode": dealercode,
        "add_date": add_date,
        "add_time": add_time,
        "edit_date": edit_date,
        "edit_time": edit_time,
        "add_tel1_ext": add_tel1_ext,
        "add_fax_ext": add_fax_ext,
        "vender_type": vender_type,
        "add_phone": add_phone,
        "sap_no": sap_no
    }
    axios.post('http://localhost:3050/api/updete', updataData)
    .then(()=>{
        const router = useRouter()
            router.push('/')
    })
}

</script>