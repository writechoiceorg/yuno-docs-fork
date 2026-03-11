---
title: Choose the Right Integration for You
deprecated: false
hidden: false
metadata:
  robots: index
---
Within each platform's SDK, Yuno offers various **integration methods** allowing varying degrees of control over the UI and user experience.

The integration method you select affects the level of maintenance effort required, the ease of managing payment methods (which may range from no-code configuration in the Yuno Dashboard to hands-on developer work), and your compliance obligations, since some integration types require certifications such as **PCI-DSS** or **ISO**.

> 👍 Recommended Integration
>
> We recommend using **Full Checkout** for the most straightforward solution with pre-built UI and automatic payment method display. It covers the most common scenarios with the least integration effort.

## Integration Types

Below, you can see the specifications for each integration type.

<HTMLBlock>{\`
<style>  
  thead th {
    background-color: #FCFCFF !important;
    border-color: #ECEFF2 !important;
    color: #282A30 !important;
    font-weight: 400 !important;
    border-width: 1px !important;
    border: none !important; 
    
  }
  
  table tr td {
    background-color: #FFFFFF !important;
    border-color: #ECEFF2 !important;
    color: #282A30 !important;
    font-weight: 400 !important;
    border-width: 1px !important;
    border: none !important; 
  }
  
  thead tr {
    border: 1px solid #ECEFF2 !important;
  }
  
  thead tr,
  tbody tr{
    height: 48px;
  }
  
  table {
    border-collapse: collapse !important; /* This ensures no spacing between table cells */
    border-color: #ECEFF2 !important;
    border-width: 1px !important;
  }
  
  table tr td:not(:first-child){
    text-align: center !important;
  }
  table tr th:not(:first-child){
    text-align: center !important;
  }
</style>
\`}</HTMLBlock>

<HTMLBlock>{\`
<table>
  <thead>
    <tr>
      <th>Feature</th>
      <th><a href="#full-checkout">Full Checkout</a></th>
      <th><a href="#secure-fields">Secure Fields</a></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Add new payment methods without code</td>
      <td><svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="#29d99a" viewBox="0 0 256 256"><path d="M128,24A104,104,0,1,0,232,128,104.11,104.11,0,0,0,128,24Zm45.66,85.66-56,56a8,8,0,0,1-11.32,0l-24-24a8,8,0,0,1,11.32-11.32L112,148.69l50.34-50.35a8,8,0,0,1,11.32,11.32Z"></path></svg></td>
      <td><svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="#f13f5e" viewBox="0 0 256 256"><path d="M128,24A104,104,0,1,0,232,128,104.11,104.11,0,0,0,128,24Zm37.66,130.34a8,8,0,0,1-11.32,11.32L128,139.31l-26.34,26.35a8,8,0,0,1-11.32-11.32L116.69,128,90.34,101.66a8,8,0,0,1,11.32-11.32L128,116.69l26.34-26.35a8,8,0,0,1,11.32,11.32L139.31,128Z"></path></svg></td>
    </tr>
    <tr>
      <td>Handle hundreds of payment methods with a single API</td>
      <td><svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="#29d99a" viewBox="0 0 256 256"><path d="M128,24A104,104,0,1,0,232,128,104.11,104.11,0,0,0,128,24Zm45.66,85.66-56,56a8,8,0,0,1-11.32,0l-24-24a8,8,0,0,1,11.32-11.32L112,148.69l50.34-50.35a8,8,0,0,1,11.32,11.32Z"></path></svg></td>
      <td><svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="#29d99a" viewBox="0 0 256 256"><path d="M128,24A104,104,0,1,0,232,128,104.11,104.11,0,0,0,128,24Zm45.66,85.66-56,56a8,8,0,0,1-11.32,0l-24-24a8,8,0,0,1,11.32-11.32L112,148.69l50.34-50.35a8,8,0,0,1,11.32,11.32Z"></path></svg></td>
    </tr>
    <tr>
      <td>Tokenize cards and payment methods without code</td>
      <td><svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="#29d99a" viewBox="0 0 256 256"><path d="M128,24A104,104,0,1,0,232,128,104.11,104.11,0,0,0,128,24Zm45.66,85.66-56,56a8,8,0,0,1-11.32,0l-24-24a8,8,0,0,1,11.32-11.32L112,148.69l50.34-50.35a8,8,0,0,1,11.32,11.32Z"></path></svg></td>
      <td><svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="#29d99a" viewBox="0 0 256 256"><path d="M128,24A104,104,0,1,0,232,128,104.11,104.11,0,0,0,128,24Zm45.66,85.66-56,56a8,8,0,0,1-11.32,0l-24-24a8,8,0,0,1,11.32-11.32L112,148.69l50.34-50.35a8,8,0,0,1,11.32,11.32Z"></path></svg></td>
    </tr>
    <tr>
      <td>Use Yuno's PCI-DSS Certification</td>
      <td><svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="#29d99a" viewBox="0 0 256 256"><path d="M128,24A104,104,0,1,0,232,128,104.11,104.11,0,0,0,128,24Zm45.66,85.66-56,56a8,8,0,0,1-11.32,0l-24-24a8,8,0,0,1,11.32-11.32L112,148.69l50.34-50.35a8,8,0,0,1,11.32,11.32Z"></path></svg></td>
      <td><svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="#29d99a" viewBox="0 0 256 256"><path d="M128,24A104,104,0,1,0,232,128,104.11,104.11,0,0,0,128,24Zm45.66,85.66-56,56a8,8,0,0,1-11.32,0l-24-24a8,8,0,0,1,11.32-11.32L112,148.69l50.34-50.35a8,8,0,0,1,11.32,11.32Z"></path></svg></td>
    </tr>
    <tr>
      <td>Use 3D Secure</td>
      <td><svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="#29d99a" viewBox="0 0 256 256"><path d="M128,24A104,104,0,1,0,232,128,104.11,104.11,0,0,0,128,24Zm45.66,85.66-56,56a8,8,0,0,1-11.32,0l-24-24a8,8,0,0,1,11.32-11.32L112,148.69l50.34-50.35a8,8,0,0,1,11.32,11.32Z"></path></svg></td>
      <td><svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="#29d99a" viewBox="0 0 256 256"><path d="M128,24A104,104,0,1,0,232,128,104.11,104.11,0,0,0,128,24Zm45.66,85.66-56,56a8,8,0,0,1-11.32,0l-24-24a8,8,0,0,1,11.32-11.32L112,148.69l50.34-50.35a8,8,0,0,1,11.32,11.32Z"></path></svg></td>
    </tr>
    <tr>
      <td>Use an antifraud solution without code</td>
      <td><svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="#29d99a" viewBox="0 0 256 256"><path d="M128,24A104,104,0,1,0,232,128,104.11,104.11,0,0,0,128,24Zm45.66,85.66-56,56a8,8,0,0,1-11.32,0l-24-24a8,8,0,0,1,11.32-11.32L112,148.69l50.34-50.35a8,8,0,0,1,11.32,11.32Z"></path></svg></td>
      <td><svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="#29d99a" viewBox="0 0 256 256"><path d="M128,24A104,104,0,1,0,232,128,104.11,104.11,0,0,0,128,24Zm45.66,85.66-56,56a8,8,0,0,1-11.32,0l-24-24a8,8,0,0,1,11.32-11.32L112,148.69l50.34-50.35a8,8,0,0,1,11.32,11.32Z"></path></svg></td>
    </tr>
    <tr>
      <td>Set checkout conditions using our dashboard</td>
      <td><svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="#29d99a" viewBox="0 0 256 256"><path d="M128,24A104,104,0,1,0,232,128,104.11,104.11,0,0,0,128,24Zm45.66,85.66-56,56a8,8,0,0,1-11.32,0l-24-24a8,8,0,0,1,11.32-11.32L112,148.69l50.34-50.35a8,8,0,0,1,11.32,11.32Z"></path></svg></td>
      <td><svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="#f13f5e" viewBox="0 0 256 256"><path d="M128,24A104,104,0,1,0,232,128,104.11,104.11,0,0,0,128,24Zm37.66,130.34a8,8,0,0,1-11.32,11.32L128,139.31l-26.34,26.35a8,8,0,0,1-11.32-11.32L116.69,128,90.34,101.66a8,8,0,0,1,11.32-11.32L128,116.69l26.34-26.35a8,8,0,0,1,11.32,11.32L139.31,128Z"></path></svg></td>
    </tr>
    <tr>
      <td>Customize the look and feel of your checkout using our dashboard</td>
      <td><svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="#29d99a" viewBox="0 0 256 256"><path d="M128,24A104,104,0,1,0,232,128,104.11,104.11,0,0,0,128,24Zm45.66,85.66-56,56a8,8,0,0,1-11.32,0l-24-24a8,8,0,0,1,11.32-11.32L112,148.69l50.34-50.35a8,8,0,0,1,11.32,11.32Z"></path></svg></td>
      <td><svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="#f13f5e" viewBox="0 0 256 256"><path d="M128,24A104,104,0,1,0,232,128,104.11,104.11,0,0,0,128,24Zm37.66,130.34a8,8,0,0,1-11.32,11.32L128,139.31l-26.34,26.35a8,8,0,0,1-11.32-11.32L116.69,128,90.34,101.66a8,8,0,0,1,11.32-11.32L128,116.69l26.34-26.35a8,8,0,0,1,11.32,11.32L139.31,128Z"></path></svg></td>
    </tr>
  </tbody>
</table>
\`}</HTMLBlock>

### Full Checkout

Our most comprehensive integration solution. It streamlines implementation, reduces maintenance and operational overhead, and removes the need to handle compliance, all while offering maximum flexibility.

* **User experience management**: Yuno manages the user experience while allowing you to customize the checkout to match your brand.
* **Payment method configuration**: Add and configure payment methods directly from the dashboard, with no extra coding.
* **Flexibility and simplicity**: Ideal for businesses that want full control over the experience without managing backend complexity.

### Secure Fields

A secure and seamless checkout solution using prebuilt UI components (Web Only):

* **Secure data collection**: Simplifies the process of collecting and tokenizing payment card details.
* **PCI compliance**: Ensures a PCI-compliant experience while maintaining a customized UI.
* **Balanced solution**: Ideal for businesses looking for a balance between security and flexibility.
