<template>
    <div class="statistic">
        <div class="row">
            <div class="col-12 admin d-flex">
                <div class="avatar">
                    <img src="/images/avatar.png" alt="" />
                </div>
                <div class="name">Максим Белоусов</div>
            </div>
        </div>
        <div class="row">
            <div
                class="col-12 d-flex justify-content-between align-items-center"
            >
                <div class="photo">
                    <img :src="activeSet.photo" alt="" class="image-set" />
                </div>
                <button
                    class="btn-back"
                    @click.prevent="$router.push('/sets/' + activeSet.id)"
                >
                    Назад
                </button>
            </div>
        </div>
        <div class="row mt-3">
            <div class="col-4">{{ activeSet.name }}</div>
            <div class="col-4">Текущая неделя:2</div>
            <div class="col-4">Итоговая оценка:</div>
        </div>
        <div class="row mt-3">
            <div class="col-12">
                <table class="table table-bordered">
                    <thead>
                        <tr>
                            <th scope="col">Недели</th>
                            <th scope="col">Оценки</th>
                            <th scope="col">Отчет</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>4</td>
                            <td>
                                <b-button class="link" v-b-modal.modal-report>
                                    link</b-button
                                >
                            </td>
                        </tr>
                    </tbody>
                </table>
                <b-modal
                    centered
                    hide-header
                    ok-only
                    ok-title="Ок"
                    id="modal-report"
                >
                    <div class="view-report">
                        <div>
                            <div class="text">Коментарий</div>
                            <div class="comment">fewrvwedvdsvfewrgvesdv</div>
                        </div>
                        <div>
                            <div class="mark mb-5">Оценка: 5 отлично</div>
                            <input type="file" />
                        </div>
                        <div
                            class="close"
                            @click="$bvModal.hide('modal-report')"
                        >
                            <img src="/images/close-modal.svg" alt="" />
                        </div>
                    </div>
                </b-modal>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data: function () {
        return {
            activeSet: {
                id: 22,
                name: "Зимний набор1",
                photo: "/images/set1.png",
                description: "vxcvxcvxc",
                startData: "01.01.2021",
                endData: "31.03.2021",
                active: true,
                startup: [
                    {
                        id: 32,
                        name: "Цифровой баян1",
                        photo: "/images/startup1.png",
                        own: "dfsdfd",
                        description: "dsfdsf",
                        target: "sdfsd",
                        plancommercial: "dsfsd",
                        planGrow: "dsfsd",
                        area: "sdfds",
                        tasks: "sfsd",
                    },
                    {
                        id: 12,
                        name: "Цифровой баян3",
                        photo: "/images/startup1.png",
                        own: "dfsdfd",
                        description: "dsfdsf",
                        target: "sdfsd",
                        plancommercial: "dsfsd",
                        planGrow: "dsfsd",
                        area: "sdfds",
                        tasks: "sfsd",
                    },
                ],
            },
        };
    },
};
</script>
<style scoped>
.statistic {
    margin-top: 30px;
    font-family: Roboto;
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 21px;
    color: #000000;
}
.name {
    font-family: Futura PT;
    font-size: 18px;
    line-height: 115%;

    color: #77797d;
}
.admin {
    align-items: center;
    justify-content: flex-end;
    margin-bottom: 50px;
}
.admin .avatar {
    margin-right: 10px;
}
.btn-back {
    background: #c4c4c4;
    border: none;
    font-family: Roboto;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    line-height: 19px;
    color: #000000;
    width: 100px;
    height: 35px;
}
.image-set {
    background: #c4c4c4;
    background-size: auto;
    border: 1px solid #000000;
    border-radius: 50%;
    width: 120px;
    height: 120px;
    margin-right: 5px;
}
.table {
    text-align: center;
    margin-left: 5%;
    width: 90%;
}
.link {
    background: transparent;
    border: none;
    color: #000000;
    padding: 0;
}
.view-report {
    display: flex;
    justify-content: space-between;
}
.view-report .close {
    position: absolute;
    top: 10px;
    right: 10px;
}
.view-report .text {
    font-family: Roboto;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    line-height: 19px;
    color: #000000;
}
.view-report .comment {
    font-family: Roboto;
    font-style: normal;
    font-weight: normal;
    font-size: 14px;
    line-height: 16px;

    color: #000000;
    margin-top: 15px;
}
</style>