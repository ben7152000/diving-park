<template>
  <div class="container my-4">
    <div class="row">
      <div class="filter col-3 border rounded-0" style="height: 100%">
        <!--  基本選項  -->
        <h4 class="title">基本選項</h4>

        <!--  地點  -->
        <div>
          <b-button
            :class="visible1 ? null : 'collapsed'"
            :aria-expanded="visible1 ? 'true' : 'false'"
            class="box-button"
            @click="visible1 = !visible1"
          >
            地點
          </b-button>
          <b-collapse v-model="visible1" class="mt-2">
            <b-card>
              <b-form-group v-slot="{ ariaDescribedby }">
                <b-form-checkbox-group
                  v-model="selected"
                  :aria-describedby="ariaDescribedby"
                  stacked
                >
                  <b-form-checkbox value="北部">北部</b-form-checkbox>
                  <b-form-checkbox value="南部">南部</b-form-checkbox>
                  <b-form-checkbox value="外島">外島</b-form-checkbox>
                </b-form-checkbox-group>
              </b-form-group>
            </b-card>
          </b-collapse>
        </div>

        <!--  難易度  -->
        <div>
          <b-button
            :class="visible2 ? null : 'collapsed'"
            :aria-expanded="visible2 ? 'true' : 'false'"
            class="box-button"
            @click="visible2 = !visible2"
          >
            難易度
          </b-button>
          <b-collapse v-model="visible2" class="mt-2">
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
        </div>

        <!--  擁有證照  -->
        <div>
          <b-button
            :class="visible3 ? null : 'collapsed'"
            :aria-expanded="visible3 ? 'true' : 'false'"
            class="box-button"
            @click="visible3 = !visible3"
          >
            擁有證照
          </b-button>
          <b-collapse v-model="visible3" class="mt-2">
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
        </div>

        <!--  高級選項  -->
        <h6 class="subtitle">高級選項</h6>

        <!--  廁所  -->
        <div>
          <b-button
            :class="visible4 ? null : 'collapsed'"
            :aria-expanded="visible3 ? 'true' : 'false'"
            class="box-button"
            @click="visible4 = !visible4"
          >
            廁所
          </b-button>
          <b-collapse v-model="visible4" class="mt-2">
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
        </div>

        <!--  盥洗  -->
        <div>
          <b-button
            :class="visible5 ? null : 'collapsed'"
            :aria-expanded="visible5 ? 'true' : 'false'"
            class="box-button"
            @click="visible5 = !visible5"
          >
            盥洗
          </b-button>
          <b-collapse v-model="visible5" class="mt-2">
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
        </div>

        <!--  最大深度  -->
        <div>
          <b-button
            :class="visible6 ? null : 'collapsed'"
            :aria-expanded="visible6 ? 'true' : 'false'"
            class="box-button"
            @click="visible6 = !visible6"
          >
            最大深度
          </b-button>
          <b-collapse v-model="visible6" class="mt-2">
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
      </div>

      <!--   卡片   -->
      <div v-if="selected.length === 0" class="col-9">
        <b-card
          v-for="(data, index) in divingData"
          :key="index"
          no-body
          class="overflow-hidden"
          style="max-width: 100%; margin-bottom: 10px"
        >
          <b-row no-gutters>
            <b-col md="4">
              <DivingImage :image="data.image" />
            </b-col>
            <b-col md="8">
              <b-card-body :title="data.title">
                <DivingText
                  :description="data.description"
                  :max-depth="data.maxDepth"
                  :visibility="data.visibility"
                  :location="data.location"
                  :degree="data.degree"
                  :license="data.license"
                  :toilet="data.toilet"
                  :bathroom="data.bathroom"
                />
              </b-card-body>
            </b-col>
          </b-row>
        </b-card>
      </div>

      <div v-else class="col-9">
        <b-card
          v-for="(data, index) in filterData"
          :key="index"
          no-body
          class="overflow-hidden"
          style="max-width: 100%; margin-bottom: 10px"
        >
          <b-row no-gutters>
            <b-col md="4">
              <DivingImage :image="data.image" />
            </b-col>
            <b-col md="8">
              <b-card-body :title="data.title">
                <DivingText
                  :description="data.description"
                  :max-depth="data.maxDepth"
                  :visibility="data.visibility"
                  :location="data.location"
                  :degree="data.degree"
                  :license="data.license"
                  :toilet="data.toilet"
                  :bathroom="data.bathroom"
                />
              </b-card-body>
            </b-col>
          </b-row>
        </b-card>
      </div>
    </div>
  </div>
</template>

<script>
import DivingImage from './Components/DivingImage'
import DivingText from './Components/DivingText'

export default {
  name: 'FilterCondition',
  components: {
    DivingImage,
    DivingText,
  },
  data() {
    return {
      selected: [],
      visible1: false,
      visible2: false,
      visible3: false,
      visible4: false,
      visible5: false,
      visible6: false,

      // diving cards
      divingData: [
        {
          image: 'https://picsum.photos/250/250/?image=20',
          title: '龍洞四號',
          description: '適合新手, 生物多樣, 豐富地形, 商家林立, 停車方便',
          maxDepth: '26',
          visibility: '1~8',
          location: '北部',
          degree: '簡單',
          license: ['初級潛水員證照', '進階潛水員證照', '救援潛水員證照'],
          toilet: true,
          bathroom: true,
        },
        {
          image: 'https://picsum.photos/250/250/?image=21',
          title: '潮境公園',
          description: '適合進階, 生物多樣, 豐富地形, 停車方便, 海底景觀豐富',
          maxDepth: '29',
          visibility: '1~8',
          location: '北部',
          degree: '普通',
          license: ['初級潛水員證照', '進階潛水員證照', '救援潛水員證照'],
          toilet: true,
          bathroom: true,
        },
        {
          image: 'https://picsum.photos/250/250/?image=22',
          title: '雙峰藍洞',
          description: '適合進階, 生物多樣, 需要船潛, 地形豐富',
          maxDepth: '29',
          visibility: '11~20',
          location: '南部',
          degree: '普通',
          license: ['進階潛水員證照', '救援潛水員證照'],
          toilet: false,
          bathroom: false,
        },
        {
          image: 'https://picsum.photos/250/250/?image=23',
          title: '滾水鼻',
          description: '適合進階, 生物多樣, 需要船潛',
          maxDepth: '40',
          visibility: '30~40',
          location: '外島',
          degree: '困難',
          license: ['進階潛水員證照', '救援潛水員證照'],
          toilet: false,
          bathroom: false,
        },
      ],
    }
  },
  computed: {
    filterData() {
      const newDivingData = []
      this.selected.forEach((i) => {
        this.divingData.forEach((j) => {
          if (i === j.location) {
            newDivingData.push(j)
          }
          if (i === j.degree) {
            newDivingData.push(j)
          }
          if (i === [...j.license]) {
            newDivingData.push(j)
          }
        })
      })

      return newDivingData
    },
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
