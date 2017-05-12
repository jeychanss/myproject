<template>
	<section>

		<el-table :data="cstm" highlight-current-row v-loading="" style="width: 100%;">
			<el-table-column prop="username" label="用户" width="300">
			</el-table-column>
			<el-table-column prop="intime" label="停入时间" width="250" >
			</el-table-column>
			<el-table-column prop="outtime" label="离开时间" width="300" >
			</el-table-column>
			<el-table-column prop="carid" label="车牌号" width="300"  sortable>
			</el-table-column>
		</el-table>
		
		<el-col :span="24" class="toolbar" >
			<el-button type="info" @click="carIn">驶入</el-button>
			<el-button type="danger" @click="carOut">驶离</el-button>
		</el-col>

		<el-dialog v-model="carInModel"	:close-on-click-modal="false">
			<el-icon-message>已驶入</el-icon-message>
		</el-dialog>	
		<el-dialog v-model="carOutModel" :close-on-click-modal="false">
			<el-icon-message>已驶出</el-icon-message>
		</el-dialog>
	</section>


</template>
<script type="text/javascript">
	export default{
		data(){
			return {
				carInModel:false,
				carOutModel:false,
				cstm: []
			}
		},
		methods:{
			getUsers(){
				this.cstm = [{
					"username":"张三",
					"intime":"2017:05:11 20:42",
					"outtime":"2017:05:11 23:12",
					"carid":"沪A20101"},
					{
					"username":"李四",
					"intime":"2017:05:11 10:42",
					"outtime":"2017:05:11 13:12",
					"carid":"苏A20101"},
				]
			},
			carIn(){
				this.carInModel=true;
			},
			carOut(){
				this.carOutModel=true;
			}
		},
		mounted(){
			this.getUsers();		
		}

	}
</script>