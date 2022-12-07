<template>
  <div class="row">
    <table class="table table-light">
      <thead>
        <tr>
          <th></th>
          <th>Date</th>
          <th>Customer Name <img src="../assets/sort-down.svg" /></th>
          <th>Amount</th>
          <th>Payment Method</th>
          <th>Products</th>
          <th>Quantity</th>
        </tr>
      </thead>
      <tbody>
        <tr class="table-desc">
          <td></td>
          <td>Today</td>
          <td colspan="5">₦78,905.00</td>
        </tr>
        <tr>
          <td class="td-checkbox">
            <input type="checkbox" class="checkbox" name="" id="" />
          </td>
          <td>
            08-Apr-22 <br />
            <span>9:34pm</span>
          </td>
          <td>Lukeman Olawale</td>
          <td class="color-red">₦4,500.00</td>
          <td>Card</td>
          <td></td>
          <td></td>
        </tr>
        <tr>
          <td class="td-checkbox">
            <input type="checkbox" class="checkbox" name="" id="" />
          </td>
          <td>
            08-Apr-22 <br />
            <span>9:34pm</span>
          </td>
          <td>
            Walex Gbadamusi
            <span>wale@gmail.com</span>
          </td>
          <td>
            <span class="color-light">₦14,500.00</span>
            <span class="color-dark">of ₦500,000.00</span>
          </td>
          <td>Bank Transfer</td>
          <td>Freezed Pie, Zinny Zip, Vintage Black</td>
          <td>38</td>
        </tr>
        <tr>
          <td class="td-checkbox">
            <input type="checkbox" class="checkbox" name="" id="" />
          </td>
          <td>
            08-Apr-22 <br />
            <span>9:34pm</span>
          </td>
          <td>Genny Mojib</td>
          <td>
            <span class="color-dark">of ₦500,000.00</span>
          </td>
          <td>Bank Transfer</td>
          <td>Dinny Zip , Vintage black</td>
          <td>27</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<style scoped>
thead tr th {
  font-size: 0.8rem;
  color: #585757;
  border-bottom: 1px solid #f0f0fe;
  font-weight: 600;
}
.table-desc {
  background: #f9f9ff;
}
.table-desc td {
  border-bottom: 1px solid #f0f0fe;
  font-size: 0.8rem;
  font-weight: 500;
}
.table td,
.table th {
  vertical-align: middle !important;
}
td {
  font-size: 0.9rem;
}
span {
  font-size: 0.7rem;
  color: #585757;
  display: block;
}
.color-red {
  color: #eb5757;
}
.color-orange {
  color: #f2994a;
}
.td-checkbox {
  position: relative;
  padding: 15px;
}
.checkbox {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
.color-light {
  color: #848484;
  font-size: 0.9rem;
}
.color-dark {
  color: #585757;
  font-size: 0.9rem;
  font-weight: 500;
}
</style>