<template>
    <section class="container">
        <h1>Demo Form</h1>
        <form @submit.prevent="handleSubmit">
            <div class="form-group">
                <label for="taiKhoan">Tài Khoản</label>
                <input type="text" class="form-control" id="taiKhoan" v-model.trim="taiKhoan">
            </div>
            <div class="form-group">
                <label for="exampleFormControlTextarea1">Bài Làm</label>
                <textarea class="form-control" id="vanMau" rows="3" v-model="vanMau"></textarea>
            </div>
            <div class="form-check">
                <input type="checkbox" class="form-check-input" id="isSave" v-model="isSave">
                <label class="form-check-label" for="exampleCheck1">Có muốn lưu Tài khoản không</label>
            </div>
            <div>
                <h1>Bạn muốn sống ở đâu ?</h1>
                <div class="form-check">
                    <input type="checkbox" class="form-check-input" v-model="noiMuonSong" value="Tp Hồ Chí Minh">
                    <label class="form-check-label">Tp Hồ Chí Minh </label>
                </div>
                <div class="form-check">
                    <input type="checkbox" class="form-check-input" v-model="noiMuonSong" value="Tp Hà Nội">
                    <label class="form-check-label">Tp Hà Nội</label>
                </div>
                <div class="form-check">
                    <input type="checkbox" class="form-check-input" v-model="noiMuonSong" value="Tp Hưng Yên">
                    <label class="form-check-label">Tp Hưng Yên</label>
                </div>
            </div>

            <div>
                <h1>Loại Người dân</h1>
                <div class="form-check">
                    <input class="form-check-input" type="radio" value="BT" v-model="loaiND">
                    <label class="form-check-label">
                        Bình thường
                    </label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" value="N" v-model="loaiND">
                    <label class="form-check-label">
                        Nghèo
                    </label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" value="CN" v-model="loaiND">
                    <label class="form-check-label">
                        Cận Nghèo
                    </label>
                </div>
            </div>

            <div class="col-auto my-1">
                <label class="mr-sm-2">Chọn lớp Học</label>
                <select class="custom-select mr-sm-2" v-model="lop">
                    <option selected>Choose...</option>
                    <option value="1">1</option>
                    <option value="2">2</option>
                    <option value="3">3</option>
                    <option value="4">4</option>
                    <option value="5">5</option>
                    <option value="6">6</option>
                    <option value="7">7</option>
                    <option value="8">8</option>
                    <option value="9">9</option>
                    <option value="10">10</option>
                    <option value="11">11</option>
                    <option value="12">12</option>
                </select>
            </div>
            <div class="form-group">
                <label for="age">Age</label>
                <input type="text" class="form-control" id="age" v-model.number="age">
            </div>
            <button type="submit" class="btb btn-success">Submit</button>
        </form>
    </section>
</template>

<script>
export default {
    data() {
        return {
            taikhoan: "",
            vanMau: "Đề bài : viết cảm nghĩ về js",
            isSave: false,
            noiMuonSong: [],
            loaiND: [],
            lop: 1,
            age: "1",
        };
    },
    methods: {
        handleSubmit() {
            console.log(this.taiKhoan);
            console.log(this.vanMau);
            console.log(this.isSave);
            console.log(this.noiMuonSong);
            console.log(this.loaiND);
            console.log(this.lop);
            console.log(typeof this.age);
        },
    },
};
</script>

<style></style>