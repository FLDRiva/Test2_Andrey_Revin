<template>
  <div class="container-table">
    <table class="table">
      <thead>
        <tr class="title-table">
          <th
            scope="col"
            style="
              border-top-left-radius: 10px;
              border-bottom-left-radius: 10px;
            "
          >
            Business Name
          </th>
          <th scope="col">
            <div class="team">
              Team
              <ui-select />
            </div>
          </th>
          <th scope="col">
            <div class="role">
              Role
              <ui-select />
            </div>
          </th>
          <th scope="col">Gmail</th>
          <th scope="col">
            <div class="brithday">
              Birthday
              <ui-select />
            </div>
          </th>
          <th scope="col">Telegram</th>
          <th scope="col">Last Login</th>
          <th scope="col" style="border: none">User permissions</th>
          <th
            scope="col"
            style="
              border: none;
              border-top-right-radius: 10px;
              border-bottom-right-radius: 10px;
            "
          ></th>
        </tr>
      </thead>

      <tbody>
        <tr v-for="item in TableName" :key="item.name" class="item-name">
          <td>
            <user-info :label="item.name" :image="item.img" />
          </td>
          <td>
            {{ item.team }}
          </td>
          <td>
            {{ item.role }}
          </td>
          <td>
            {{ item.gmail }}
          </td>
          <td>
            {{ item.brithday }}
          </td>
          <td>
            {{ item.tg }}
          </td>
          <td>
            {{ item.lastLogin }}
          </td>
          <td>
            <edit-button :label="'Edit'" />
          </td>
          <td>
            <ui-trash />
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import EditButton from "../components/EditButton.vue";
import UiTrash from "../components/UiTrash.vue";
import UiSelect from "../components/UiSelect.vue";
import UserInfo from "../components/UserInfo.vue";

export default {
  data() {
    return {
      TableName: [
        {
          name: "Sarah Connor",
          team: "Crosty",
          role: "Team Lead",
          gmail: "sarahconnor@gmail.com",
          brithday: "25.04.1994",
          tg: "@sarahconnor",
          lastLogin: "03.11.2021",
          img: "sara.png",
        },
        {
          name: "Arnold Brown",
          team: "Gunters",
          role: "Seo Specialist",
          gmail: "arnoldbrown@gmail.com",
          brithday: "12.04.1989",
          tg: "@arnoldbrown",
          lastLogin: "02.11.2021",
          img: "arnold.png",
        },
        {
          name: "Ernest Eberly",
          team: "Flamethrower",
          role: "Semantic Specialist",
          gmail: "ernesteberly@gmail.com",
          brithday: "17.06.1993",
          tg: "@ErnestEberly",
          lastLogin: "03.11.2021",
          img: "ernest.png",
        },
        {
          name: "Lance Thomas",
          team: "Wizards",
          role: "Seo Specialist",
          gmail: "lancethomas@gmail.com",
          brithday: "12.04.1989",
          tg: "@LanceThomas",
          lastLogin: "01.11.2021",
          img: "lance.png",
        },
        {
          name: "Cheryl Glover",
          team: "Gunters",
          role: "Python Programmist",
          gmail: "cherylglover@gmail.com",
          brithday: "15.08.1985",
          tg: "@CherylGlover",
          lastLogin: "03.11.2021",
          img: "cheryl.png",
        },
        {
          name: "Lance Thomas",
          team: "Crosty",
          role: "Seo Specialist",
          gmail: "lancethomas@gmail.com",
          brithday: "12.04.1989",
          tg: "@LanceThomas",
          lastLogin: "01.11.2021",
          img: "lance2.png",
        },
        {
          name: "Ernest Eberly",
          team: "Flamethrower",
          role: "Semantic Specialist",
          gmail: "ernesteberly@gmail.com",
          brithday: "17.06.1993",
          tg: "@ErnestEberly",
          lastLogin: "03.11.2021",
          img: "ernest.png",
        },
        {
          name: "Lance Thomas",
          team: "Wizards",
          role: "Seo Specialist",
          gmail: "lancethomas@gmail.com",
          brithday: "12.04.1989",
          tg: "@LanceThomas",
          lastLogin: "01.11.2021",
          img: "lance.png",
        },
      ],
    };
  },
  components: {
    EditButton,
    UiTrash,
    UiSelect,
    UserInfo,
  },
};
</script>

<style lang="scss" scoped>
.container-table {
  display: flex;
  font-family: Commissioner;
  background: #fff;
  border-radius: 18px;
  height: calc(100% - 79px - 48px - 68px - 28px - 28px - 28px - 28px);
  overflow: hidden;
  padding: 16px;
  box-sizing: border-box;

  .table {
    width: 100%;
    padding: 16px;
    border-collapse: collapse;
    .title-table {
      background: rgba(245, 247, 251, 1);
      height: 64px;
      text-align: left;
      font-weight: 500;
      font-size: 12px;
      line-height: 15.6px;
      color: rgba(42, 53, 90, 1);
      th {
        padding: 22px 16px 22px 16px;
        border-right: 1px solid rgba(229, 232, 239, 1);
      }
      .item-name {
        display: flex;
        gap: 3vh;
        margin-top: 5vh;
        text-align: left;
        font-weight: 400;
        font-size: 14px;
        line-height: 20px;
      }
    }
  }
  .team,
  .role,
  .brithday {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }

  table {
    border-collapse: collapse;
    margin: 0;
    padding: 0;
    width: 100%;
    table-layout: fixed;

    tr {
      background-color: #f8f8f8;
      border-bottom: 1px solid rgb(245, 247, 251);
    }

    th,
    td {
      text-align: center;
      word-wrap: break-word;
      font-size: 14px;
    }
  }
}
</style>
