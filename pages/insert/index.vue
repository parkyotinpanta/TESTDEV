<template>
    <div>
        <v-text-field v-model="dataInsert.branch_no" label="เลขสาขา"></v-text-field>
        <v-text-field v-model="dataInsert.pre_name" label="ข้อมูลผู้จำหน่าย"></v-text-field>
        <v-text-field v-model="dataInsert.ven_code" label="เลขประจำตัวผู้เสียภาษี"></v-text-field>
        <v-text-field v-model="dataInsert.ven_name" label="นามสกุล"></v-text-field>
        <v-text-field v-model="dataInsert.contact_name" label="ชื่อผู้ติดต่อ"></v-text-field>
        <v-text-field v-model="dataInsert.add_name" label="สถานที่ตั้ง"></v-text-field>
        <v-text-field v-model="dataInsert.add_no" label="เลขที่"></v-text-field>
        <v-text-field v-model="dataInsert.add_moo" label="หมู่"></v-text-field>
        <v-text-field v-model="dataInsert.add_soi" label="ตรอก"></v-text-field>
        <v-text-field v-model="dataInsert.add_trog" label="ซอย"></v-text-field>
        <v-text-field v-model="dataInsert.add_road" label="ถนน"></v-text-field>
        <v-text-field v-model="dataInsert.add_tumbol" label="แขวง/ตำบล"></v-text-field>
        <v-text-field v-model="dataInsert.add_amphur" label="อำเภอ/เขต"></v-text-field>
        <v-text-field v-model="dataInsert.add_provid" label="จังหวัด"></v-text-field>
        <v-text-field v-model="dataInsert.add_province" label="ภาค"></v-text-field>
        <v-text-field v-model="dataInsert.add_zip" label="รหัสไปรษณีย์"></v-text-field>
        <v-text-field v-model="dataInsert.add_tel" label="ติดต่อ"></v-text-field>
        <v-text-field v-model="dataInsert.add_fax_ext" label="แฟกซ์"></v-text-field>
        <v-text-field v-model="dataInsert.add_email" label="อีเมล"></v-text-field>
        <v-text-field v-model="dataInsert.vengroup_code" label="ประเภทการสั่งซื้อ"></v-text-field>
        <v-text-field v-model="dataInsert.vat_type" label="ประเภทภาษี"></v-text-field>
        <v-text-field v-model="dataInsert.vat_code" label="จำนวน"></v-text-field>
        <v-text-field v-model="dataInsert.ven_discount" label="การลดราคา"></v-text-field>
        <v-text-field v-model="dataInsert.ven_ship_term" label="ระยะเวลาจัดส่ง"></v-text-field>
        <v-text-field v-model="dataInsert.ven_ct_code" label="เลขของพัสถุ"></v-text-field>
        <v-text-field v-model="dataInsert.ven_credit_term" label="เครดิต"></v-text-field>
        <v-text-field v-model="dataInsert.ven_balance" label="งบ"></v-text-field>
        <v-text-field v-model="dataInsert.contact_fdate" label="ติดต่อล่าสุด"></v-text-field>
        <v-text-field v-model="dataInsert.contact_ldate" label="วันยกเลิกที่ติดต่อ"></v-text-field>
        <v-text-field v-model="dataInsert.cancel_date" label="ยกเลิกข้อมูล"></v-text-field>
        <v-text-field v-model="dataInsert.rec_memo" label="บันทึกช่วยจำ"></v-text-field>
        <v-text-field v-model="dataInsert.ordering_date" label="ข้อมูล"></v-text-field>
        <v-text-field v-model="dataInsert.ordering_cycle" label="รอบสั่งซื้อ"></v-text-field>
        <v-text-field v-model="dataInsert.AF_Status" label="สถานะ"></v-text-field>
        <v-text-field v-model="dataInsert.ven_balance_cs" label="ภาษี"></v-text-field>
        <v-text-field v-model="dataInsert.tax_id" label="ที่อยู่ของผู้จำหน่าย"></v-text-field>
        <v-text-field v-model="dataInsert.tax_branch_id" label="ไอดีผู้จำหน่าย"></v-text-field>
        <v-text-field v-model="dataInsert.tax_branch" label="ข้อมูลผู้จำหน่าย"></v-text-field>
        <v-text-field v-model="dataInsert.dealercode" label="รหัสตัวแทนจำหน่าย"></v-text-field>
        <v-text-field v-model="dataInsert.add_date" label="วันที่"></v-text-field>
        <v-text-field v-model="dataInsert.add_time" label="เวลา"></v-text-field>
        <v-text-field v-model="dataInsert.edit_date" label="วันที่"></v-text-field>
        <v-text-field v-model="dataInsert.edit_time" label="เวลา"></v-text-field>
        <v-text-field v-model="dataInsert.add_tel1_ext" label="พิม"></v-text-field>
        <v-text-field v-model="dataInsert.vender_type" label="เบอร์โทรศัพท์"></v-text-field>
        <v-text-field v-model="dataInsert.add_phone" label="หมายเหตุ"></v-text-field>
        <v-text-field v-model="dataInsert.sap_no" label="เครดิต"></v-text-field>
        <v-text-field v-model="dataInsert.ven_credit_limit" label="เครดิต"></v-text-field>

        <v-btn color="green-darken-3" @click="insert(dataInsert)">บันทึก</v-btn>

    </div>
</template>
<script setup>
import axios from 'axios';
import { useRoute } from 'nuxt/app'
const dataInsert = ref({
    branch_no: 0,
    pre_name: "",
    ven_code: "",
    ven_name: "",
    contact_name: "",
    add_name: "",
    add_no: "",
    add_moo: "",
    add_soi: "",
    add_trog: "",
    add_road: "",
    add_tumbol: "",
    add_amphur: "",
    add_provid: "",
    add_province: 0,
    add_zip: "",
    add_tel: "",
    add_fax_ext: "",
    add_email: "",
    vengroup_code: "",
    vat_type: "",
    vat_code: "",
    ven_discount: 0,
    ven_ship_term: 0,
    ven_ct_code: "",
    ven_credit_term: 0,
    ven_balance: 0,
    contact_fdate: "",
    contact_ldate: "",
    cancel_date: 0,
    rec_memo: "",
    ordering_date: 0,
    ordering_cycle: 0,
    AF_Status: "",
    ven_balance_cs: 0,
    tax_id: "",
    tax_branch_id: "",
    tax_branch: "",
    dealercode: "",
    add_date: "",
    add_time: "",
    edit_date: "",
    edit_time: "",
    add_tel1_ext: "",
    vender_type: "",
    add_phone: "",
    sap_no: "",
    ven_credit_limit: 0
})

function insert(item) {
    let { branch_no, pre_name, ven_code, ven_name, contact_name, add_name, add_no, add_moo
        , add_soi, add_trog, add_road, add_tumbol, add_amphur, add_provid, add_province
        , add_zip, add_tel, add_fax_ext, add_email, vengroup_code, vat_type, vat_code
        , ven_discount, ven_ship_term, ven_ct_code, ven_credit_term, ven_balance
        , contact_fdate, contact_ldate, cancel_date, rec_memo, ordering_date
        , ordering_cycle, AF_Status, ven_balance_cs, tax_id, tax_branch_id
        , tax_branch, dealercode, add_date, add_time, edit_date, edit_time
        , add_tel1_ext, vender_type, add_phone, sap_no, ven_credit_limit } = item
    let insertData = {
        "branch_no": branch_no,
        "ven_code": ven_code,
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
        "add_fax_ext": add_fax_ext,
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
        "vender_type": vender_type,
        "add_phone": add_phone,
        "sap_no": sap_no
    }

    axios.post('http://localhost:3050/api/insert', insertData)
        .then((item) => {
            const router = useRouter()
            router.push('/')

        })




}


</script>





