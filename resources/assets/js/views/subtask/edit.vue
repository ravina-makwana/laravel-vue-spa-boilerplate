<template>
	<div>
        <div class="row page-titles">
            <div class="col-md-12 col-8 align-self-center">
                <h3 class="text-themecolor m-b-0 m-t-0">Edit Task</h3>
                <ol class="breadcrumb">
                    <li class="breadcrumb-item"><router-link to="/home">Home</router-link></li>
                    <li class="breadcrumb-item"><router-link :to="{name: 'subtask.index'}">SubTask</router-link></li>
                    <li class="breadcrumb-item active">Edit Task</li>
                </ol>
            </div>
        </div>
        
        <div class="row">
            <div class="col-sm-12">
                <div class="card">
                    <div class="card-body">
                        <h4 class="card-title">Edit Task</h4>
                        <sub-task-form :id="id"></sub-task-form>
                    </div>
                </div>
            </div>
        </div>
    </div>	
</template>

<script>
	import SubTaskForm from './form'
	import helper from '../../services/helper'

	export default {
		name: 'subtask-edit',
		components: { SubTaskForm },
		data() {
			return {
				id: this.$route.params.id
			}
		}
	}
</script>