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
