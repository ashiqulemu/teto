<template>
    <div class="array-input">
        <div class="row">
            <div class="col-md-6">
                <div class="form-group">
                    <label >Teach</label>
                    <v-select
                            taggable
                            name="subject"
                            v-model="subject"
                            :options="['foo','bar']"
                            id="subject"
                    ></v-select>
                </div>
            </div>
            <div class="col-md-2">
                <div class="form-group">
                    <label >Level</label>
                    <input type="text"
                           name="level"
                           v-model="level"
                           placeholder="GCSE"
                           class="form-control"
                    >
                </div>
            </div>
            <div class="col-md-4">
                <div class="form-group">
                    <label >Price</label>
                    <input type="number"
                           name="price"
                           v-model="price"
                           placeholder="AED 30"
                           class="form-control"
                    >
                </div>
            </div>

        </div>
        <div class="row">
            <div class="col-md-12">
                <div class="form-group">
                    <span class="another-qualification" @click="addTeach()" style="cursor: pointer">
                        <i class="fas fa-plus-circle"></i>
                        Add Teach
                    </span>
                </div>
            </div>
        </div>
            <ul class="list-group">
                <li class="list-group-item" v-for="(teach, index) in teaches">
                    {{'subject: ' + teach.subject + ', level: ' + teach.level + ', price: ' + teach.price}}
                    <button
                            class="btn btn-sm btn-danger float-right"
                            @click="deleteTeach(index)">
                        <i class="fa fa-times"></i>
                    </button>

                    <button
                            class="btn btn-sm btn-success float-right edit-btn"
                            @click="editTeach(index)">
                        <i class="fa fa-pen"></i>
                    </button>
                </li>
            </ul>

    </div>
</template>
<script src="./js/teach.js"></script>
