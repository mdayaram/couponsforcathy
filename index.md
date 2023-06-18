---
layout: default
---

<table>
  <thead>
    <tr>
      <th>Created</th>
      <th>Coupon Value</th>
      <th>Reasons</th>
      <th>Redemption Status</th>
    </tr>
  </thead>
  <tbody>
{%- for coupon in site.data.coupons -%}
    <tr>
      <td>{{ coupon.created_at }}</td>
      <td>{{ coupon.value }}</td>
      <td>{{ coupon.reason }}</td>
      <td>{{ coupon.redeemed_at | default: "Not redeemed yet." }}</td>
    </tr>
{%- endfor -%}
  </tbody>
</table>
