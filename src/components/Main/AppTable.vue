<script>
import ButtonApp from "../AppButton.vue";
export default {
  data() {
    return {
      buttonSecondary: "button_secondary",
      buttonPrimary: "button_primary",
      buttonText: "GET IN NOW",
    };
  },
  components: { ButtonApp },
};
</script>

<template>
  <table>
    <thead>
      <tr>
        <th>
          Save up to 40% <br />
          by paying weekly
        </th>
        <th class="table_bg">
          <img class="my-3" src="/img/h5-custom-icon-7.png" alt="" />
          <div>Standard</div>
          <div class="mb-3">$12</div>
        </th>
        <th class="table_bg">
          <img class="my-3" src="/img/h5-custom-icon-8.png" alt="" />
          <div>Professional</div>
          <div class="mb-3">$59</div>
        </th>
        <th class="table_bg">
          <img class="my-3" src="/img/h5-custom-icon-9.png" alt="" />
          <div>Advanced</div>
          <div class="mb-3">$88</div>
        </th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Numbers of courses</td>
        <td>2</td>
        <td>4</td>
        <td>6</td>
      </tr>
      <tr>
        <td>Time</td>
        <td>15 Days</td>
        <td>30 Days</td>
        <td>30 Days</td>
      </tr>
      <tr>
        <td>Web Designing</td>
        <td><font-awesome-icon icon="fa-solid fa-check" /></td>
        <td><font-awesome-icon icon="fa-solid fa-check" /></td>
        <td><font-awesome-icon icon="fa-solid fa-check" /></td>
      </tr>
      <tr>
        <td>Human-Centered Design</td>
        <td><font-awesome-icon icon="fa-solid fa-check" /></td>
        <td><font-awesome-icon icon="fa-solid fa-check" /></td>
        <td><font-awesome-icon icon="fa-solid fa-check" /></td>
      </tr>
      <tr>
        <td>Basic Marketing</td>
        <td><font-awesome-icon icon="fa-solid fa-xmark" /></td>
        <td><font-awesome-icon icon="fa-solid fa-check" /></td>
        <td><font-awesome-icon icon="fa-solid fa-check" /></td>
      </tr>
      <tr>
        <td>Pyhton for Everybody</td>
        <td><font-awesome-icon icon="fa-solid fa-xmark" /></td>
        <td><font-awesome-icon icon="fa-solid fa-check" /></td>
        <td><font-awesome-icon icon="fa-solid fa-check" /></td>
      </tr>
      <tr>
        <td>Android Developer</td>
        <td><font-awesome-icon icon="fa-solid fa-xmark" /></td>
        <td><font-awesome-icon icon="fa-solid fa-xmark" /></td>
        <td><font-awesome-icon icon="fa-solid fa-check" /></td>
      </tr>
      <tr>
        <td>Business English</td>
        <td><font-awesome-icon icon="fa-solid fa-xmark" /></td>
        <td><font-awesome-icon icon="fa-solid fa-xmark" /></td>
        <td><font-awesome-icon icon="fa-solid fa-check" /></td>
      </tr>
    </tbody>
    <tfoot>
      <tr>
        <td></td>
        <td class="table_bg">
          <ButtonApp :customButton="buttonSecondary" :text="buttonText" />
        </td>
        <td class="table_bg">
          <ButtonApp :customButton="buttonPrimary" :text="buttonText" />
        </td>
        <td class="table_bg">
          <ButtonApp :customButton="buttonSecondary" :text="buttonText" />
        </td>
      </tr>
    </tfoot>
  </table>
</template>

<style lang="scss" scoped>
table {
  th {
    width: 200px;
    border: 1px solid #ababab;
  }

  tr {
    border: 1px solid #ababab;
  }
  td {
    border: 1px solid #ababab;
    padding: 15px 0;
    color: #898989;
    .fa-check {
      color: #40c4ff;
    }
  }
  .table_bg {
    background-color: #f7fdff;
  }
  .button_primary {
    width: 160px;
    height: 50px;
    border: #40c4ff;
    margin: 20px auto;
    border-radius: 0;
    color: white;
    background-color: #40c4ff;
    font-size: 0.85rem;
    font-weight: 600;
    cursor: pointer;
  }

  .button_secondary {
    width: 160px;
    height: 50px;
    margin: 20px auto;
    border-radius: 0;
    background-color: white;
    border: 1px solid #ababab;
    color: #ababab;
    font-size: 0.85rem;
    font-weight: 600;
    cursor: pointer;
  }
}
</style>
