<template>
  <div class="filter">
    <!--  已選擇  -->
    <div>
      <h6>已選擇</h6>
      <span>{{ selected }}</span>
    </div>

    <!--  基本選項  -->
    <h4 class="title">基本選項</h4>

    <!--  地點  -->
    <b-button
      :class="visible1 ? null : 'collapsed'"
      :aria-expanded="visible1 ? 'true' : 'false'"
      :aria-controls="1"
      class="box-button"
      @click="visible1 = !visible1"
    >
      地點
    </b-button>
    <b-collapse :id="1" v-model="visible1" class="mt-2">
      <b-card>
        <b-form-group v-slot="{ ariaDescribedby }">
          <b-form-checkbox-group
            v-model="selected"
            :aria-describedby="ariaDescribedby"
            stacked
          >
            <b-form-checkbox value="北部">北部</b-form-checkbox>
          </b-form-checkbox-group>
        </b-form-group>
      </b-card>
    </b-collapse>

    <!--  難易度  -->
    <b-button
      :class="visible2 ? null : 'collapsed'"
      :aria-expanded="visible2 ? 'true' : 'false'"
      :aria-controls="2"
      class="box-button"
      @click="visible2 = !visible2"
    >
      難易度
    </b-button>
    <b-collapse :id="2" v-model="visible2" class="mt-2">
      <b-card>
        <b-form-group v-slot="{ ariaDescribedby }">
          <b-form-checkbox-group
            v-model="selected"
            :aria-describedby="ariaDescribedby"
            stacked
          >
            <b-form-checkbox value="簡單">簡單</b-form-checkbox>
            <b-form-checkbox value="普通">普通</b-form-checkbox>
            <b-form-checkbox value="困難">困難</b-form-checkbox>
          </b-form-checkbox-group>
        </b-form-group>
      </b-card>
    </b-collapse>

    <!--  擁有證照  -->
    <b-button
      :class="visible3 ? null : 'collapsed'"
      :aria-expanded="visible3 ? 'true' : 'false'"
      :aria-controls="3"
      class="box-button"
      @click="visible3 = !visible3"
    >
      擁有證照
    </b-button>
    <b-collapse :id="3" v-model="visible3" class="mt-2">
      <b-card>
        <b-form-group v-slot="{ ariaDescribedby }">
          <b-form-checkbox-group
            v-model="selected"
            :aria-describedby="ariaDescribedby"
            stacked
          >
            <b-form-checkbox value="初級潛水員證照"
              >初級潛水員證照 (OW)</b-form-checkbox
            >
            <b-form-checkbox value="進階潛水員證照"
              >進階潛水員證照 (AOW)</b-form-checkbox
            >
            <b-form-checkbox value="救援潛水員證照"
              >救援潛水員證照</b-form-checkbox
            >
          </b-form-checkbox-group>
        </b-form-group>
      </b-card>
    </b-collapse>

    <!--  高級選項  -->
    <h6 class="subtitle">高級選項</h6>

    <!--  廁所  -->
    <b-button
      :class="visible4 ? null : 'collapsed'"
      :aria-expanded="visible3 ? 'true' : 'false'"
      :aria-controls="4"
      class="box-button"
      @click="visible4 = !visible4"
    >
      廁所
    </b-button>
    <b-collapse :id="4" v-model="visible4" class="mt-2">
      <b-card>
        <b-form-group v-slot="{ ariaDescribedby }">
          <b-form-checkbox-group
            v-model="selected"
            :aria-describedby="ariaDescribedby"
            stacked
          >
            <b-form-checkbox value="廁所">有</b-form-checkbox>
          </b-form-checkbox-group>
        </b-form-group>
      </b-card>
    </b-collapse>

    <!--  盥洗  -->
    <b-button
      :class="visible5 ? null : 'collapsed'"
      :aria-expanded="visible5 ? 'true' : 'false'"
      :aria-controls="5"
      class="box-button"
      @click="visible5 = !visible5"
    >
      盥洗
    </b-button>
    <b-collapse :id="5" v-model="visible5" class="mt-2">
      <b-card>
        <b-form-group v-slot="{ ariaDescribedby }">
          <b-form-checkbox-group
            v-model="selected"
            :aria-describedby="ariaDescribedby"
            stacked
          >
            <b-form-checkbox value="盥洗">有</b-form-checkbox>
          </b-form-checkbox-group>
        </b-form-group>
      </b-card>
    </b-collapse>

    <!--  最大深度  -->
    <b-button
      :class="visible6 ? null : 'collapsed'"
      :aria-expanded="visible6 ? 'true' : 'false'"
      :aria-controls="6"
      class="box-button"
      @click="visible6 = !visible6"
    >
      最大深度
    </b-button>
    <b-collapse :id="6" v-model="visible6" class="mt-2">
      <b-card>
        <b-form-group v-slot="{ ariaDescribedby }">
          <b-form-checkbox-group
            v-model="selected"
            :aria-describedby="ariaDescribedby"
            stacked
          >
            <b-form-checkbox value="1~10 米">1~10 米</b-form-checkbox>
            <b-form-checkbox value="11~20 米">11~20 米</b-form-checkbox>
            <b-form-checkbox value="21~30 米">21~30 米</b-form-checkbox>
            <b-form-checkbox value="31~40 米">31~40 米</b-form-checkbox>
          </b-form-checkbox-group>
        </b-form-group>
      </b-card>
    </b-collapse>
  </div>
</template>

<script>
export default {
  name: 'FilterCondition',
  data() {
    return {
      selected: [],
      visible1: false,
      visible2: false,
      visible3: false,
      visible4: false,
      visible5: false,
      visible6: false,
    }
  },
}
</script>

<style scoped lang="scss">
.filter {
  padding: 20px 30px;

  .title {
    font-weight: bold;
    margin-bottom: 10px;
  }

  .subtitle {
    font-weight: normal;
    margin: 10px 0;
  }

  .box-button {
    width: 100px;
    margin: 10px 0;
  }
}
</style>
