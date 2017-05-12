<template>
	<section>

		<el-table :data="cstm" highlight-current-row v-loading="" style="width: 100%;">
			<el-table-column type="index" label="序号" width="80">
			</el-table-column>
			<el-table-column prop="username" label="停车用户" width="120" sortable>
			</el-table-column>
			<el-table-column prop="carid" label="车牌号" width="100"  sortable>
			</el-table-column>
			<el-table-column prop="floornum" label="历史停车楼层" width="120" >
			</el-table-column>
			<el-table-column prop="area" label="历史停车区域" width="120" 	>
			</el-table-column>
			<el-table-column prop="name" label="历史停车位号" min-width="180" sortable>
			</el-table-column>
			<el-table-column prop="intime" label="停车开始时间" min-width="180" sortable>
			</el-table-column>
			<el-table-column prop="outtime" label="停车结束时间" min-width="180" sortable>
			</el-table-column>
		</el-table>
	</section>


</template>
<script type="text/javascript">
	export default{
		data(){
			return {
				cstm: []
			}
		},
		methods:{
			getUsers(){
				this.cstm = [{
					"username":"张三",
					"carid":"苏A20101",
					"floornum":"2",
					"area":"2",
					"name":"21",
					"intime":"2017:05:10 21:20",
					"outtime":"2017:05:10 22:20"},
					{"username":"李思思",
					"carid":"沪A20101",
					"floornum":"2",
					"area":"2",
					"name":"21",
					"intime":"2017:05:10 21:20",
					"outtime":"2017:05:10 22:20"},
				]
			}
		},
		mounted(){
			this.getUsers();		
		}

	}
</script>