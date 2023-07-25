---
layout: default
---

# [Digital] Coupons for Cathy

Cathy keeps losing her coupons and complaining that Manoj doesn't accept photos
of them, so we are now forced to go digital. Below is a list of all coupons that
Cathy has from Manoj.


<table>
  <thead>
    <tr>
      <th>Created</th>
      <th>From</th>
      <th>To</th>
      <th>Coupon Value</th>
      <th>Reasons</th>
      <th>Redemption Status</th>
    </tr>
  </thead>
  <tbody>
{%- for coupon in site.data.coupons -%}
    <tr>
      <td>{{ coupon.created_at }}</td>
      <td>{{ coupon.from }}</td>
      <td>{{ coupon.to }}</td>
      <td>{{ coupon.value }}</td>
      <td>{{ coupon.reason }}</td>
      <td>
        {%- if coupon.redeemed_at == null or coupon.redeemed_at == "" -%}
        <a class="redeem" href="https://github.com/mdayaram/couponsforcathy.com/issues/new?title=Redeeming {{ coupon.value }}">Redeem Now!</a>
        {%- else -%}
        Redeemed on {{ coupon.redeemed_at }}
        {%- endif -%}
      </td>
    </tr>
{%- endfor -%}
  </tbody>
</table>
