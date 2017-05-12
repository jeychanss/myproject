<template>
	<section>

		<el-table :data="cstm" highlight-current-row v-loading="" style="width: 100%;">
			<el-table-column prop="floornum" label="层数" width="300">
			</el-table-column>
			<el-table-column prop="area" label="区域" width="200" sortable>
			</el-table-column>
			<el-table-column prop="name" label="车位号" width="300"  sortable>
			</el-table-column>
			<el-table-column prop="opre" label="操作" width="350" >
				<template scope="scope">
					<el-button size="small" @click="">停入当前车位</el-button>
					<el-button type="danger" size="small" @click="">删除</el-button>
				</template>
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
					"floornum":"1",
					"area":"39",
					"name":"390"},
					{"floornum":"2",
					"area":"51",
					"name":"510"},
				]
			}
		},
		mounted(){
			this.getUsers();		
		}

	}
</script>