# @voucherify/sdk

## 2.0.4

### Patch Changes

- [`f411c1a`](https://github.com/voucherifyio/voucherify-js-sdk/commit/f411c1a56085d80560fdca634e5fdc059a556091) [#119](https://github.com/voucherifyio/voucherify-js-sdk/pull/119) Thanks [@darekg11](https://github.com/darekg11)! - Added support for stackable API methods - validation, redemptions, rollback for both Server Side and Client Side SDKs. Added some missing fields in already existing types definitions and cleaned up other definitions by reusing interfaces

## 2.0.3

### Patch Changes

- [`da9e103`](https://github.com/voucherifyio/voucherify-js-sdk/commit/da9e103a43590b55cb80d64e1743f7ede1e09946) [#117](https://github.com/voucherifyio/voucherify-js-sdk/pull/117) Thanks [@darekg11](https://github.com/darekg11)! - Added support for listing customer activities by customerId. Additionally user can pass query params allowing for better filtering. API Reference: https://docs.voucherify.io/reference/get-customer-activities

## 2.0.2

### Patch Changes

- [`b5f04fa`](https://github.com/voucherifyio/voucherify-js-sdk/commit/b5f04fa09db6849f514910747a5ac9a721f63891) [#112](https://github.com/voucherifyio/voucherify-js-sdk/pull/112) Thanks [@darekg11](https://github.com/darekg11)! - Query params passed to `this.client.post` method are now correctly stringified. Added possibility to pass query params to `voucherify.promotions.validate` method in order to allow developers using SDK to pass advanced filters to restrict possible range of promotion campaigns against which validation should be performed.

## 2.0.1

### Patch Changes

- [`532e82b`](https://github.com/voucherifyio/voucherify-js-sdk/commit/532e82b2bd3a5991a0fd83af2edc226c6c98c680) [#105](https://github.com/voucherifyio/voucherify-js-sdk/pull/105) Thanks [@jfougere](https://github.com/jfougere)! - Fix missing session attributes in client side validation request

## 2.0.0

### Major Changes

- [`c5c8b97`](https://github.com/voucherifyio/voucherify-js-sdk/commit/c5c8b97ac9aa230ed77012c2782643df7caf119b) [#93](https://github.com/voucherifyio/voucherify-js-sdk/pull/93) Thanks [@awilczek](https://github.com/awilczek)! - Support new async API methods

  Changes:

  - Campaign vouchers import
    - added CampaignsVouchersImportResponse
  - Vouchers import
    - added VouchersImportResponse
  - Vouchers bulkUpdate
    - using new API method
    - **BREAKING** change of VouchersBulkUpdateResponse
    - **BREAKING** obligatory 'metadata' field in VouchersBulkUpdateObject
  - Vouchers bulkUpdateMetadata
    - using new API method
    - **BREAKING** change of VouchersBulkUpdateMetadataResponse
    - **BREAKING** obligatory 'metadata' field in VouchersBulkUpdateMetadata
  - Products bulkUpdate
    - using [new API method](https://docs.voucherify.io/reference/post-products-in-bulk)
    - **BREAKING** change of ProductsBulkUpdateResponse
  - Products bulkUpdateMetadata
    - using [new API method](https://docs.voucherify.io/reference/async-update-products-metadata-in-bulk)
    - **BREAKING** change of method name
    - **BREAKING** change of ProductsBulkUpdateMetadataResponse
  - Products getSku
    - using [new API method](https://docs.voucherify.io/reference/get-sku-v20210726)
    - **BREAKING** change of method params
    - changed in CR fixes

## 1.3.1

### Patch Changes

- [`8ff9b8d`](https://github.com/voucherifyio/voucherify-js-sdk/commit/8ff9b8d6e2535b524b2d5707a69ffd3ced4b2254) [#95](https://github.com/voucherifyio/voucherify-js-sdk/pull/95) Thanks [@pannga](https://github.com/pannga)! - Version 1.3.0 enabled encoding in RequestController - it was used to fix encoding for both server side and client side SDKs. This introduced issue, as we did not notice that ClientSide get methods were explicitly encoding query params (toQueryParams function). That meant the query params were encoded twice and that lead to issues with characters such as %.

## 1.3.0

### Minor Changes

- [`bc0b14b`](https://github.com/voucherifyio/voucherify-js-sdk/commit/bc0b14b56c3b91896e0fbf50e040cee11b24bc4e) [#91](https://github.com/voucherifyio/voucherify-js-sdk/pull/91) Thanks [@pannga](https://github.com/pannga)! - Fixed wrong Qs arrayFormat

## 1.2.0

### Minor Changes

- [`0425e2b`](https://github.com/voucherifyio/voucherify-js-sdk/commit/0425e2b27b9bead05c828af9c6b4e369e6df2b21) [#88](https://github.com/voucherifyio/voucherify-js-sdk/pull/88) Thanks [@darekg11](https://github.com/darekg11)! - Allow to pass additional headers to requests made to Voucherify API. Custom headers can be passed via 'customHeaders' option available in VoucherifyServerSideOptions and VoucherifyClientSideOptions. Such option might prove to be useful when debugging

## 1.1.0

### Minor Changes

- [`16019cf`](https://github.com/voucherifyio/voucherify-js-sdk/commit/16019cf22b4604c609b3baac488b46a334279424) [#79](https://github.com/voucherifyio/voucherify-js-sdk/pull/79) Thanks [@mandraszyk](https://github.com/mandraszyk)! - Async Actions API support added

## 1.0.1

### Patch Changes

- [`39276e4`](https://github.com/voucherifyio/voucherify-js-sdk/commit/39276e4e5d199fe4a15e0a64f55b07949c23be30) [#74](https://github.com/voucherifyio/voucherify-js-sdk/pull/74) Thanks [@pannga](https://github.com/pannga)! - Updated changesets/cli to the latest version

* [`39276e4`](https://github.com/voucherifyio/voucherify-js-sdk/commit/39276e4e5d199fe4a15e0a64f55b07949c23be30) [#74](https://github.com/voucherifyio/voucherify-js-sdk/pull/74) Thanks [@pannga](https://github.com/pannga)! - Removed \$FixMe types

- [`0d5b2c0`](https://github.com/voucherifyio/voucherify-js-sdk/commit/0d5b2c06087f15d0bfcbd67d50ee4deaf5d9883e) [#70](https://github.com/voucherifyio/voucherify-js-sdk/pull/70) Thanks [@pannga](https://github.com/pannga)! - Updated examples and documentation.

## 1.0.0

### Major Changes

- [`2a00746`](https://github.com/voucherifyio/voucherify-js-sdk/commit/2a00746599004b6a649bc6d892e9adbd8f413f81) [#69](https://github.com/voucherifyio/voucherify-js-sdk/pull/69) Thanks [@pannga](https://github.com/pannga)! - The first major version combines previously maintained Voucherify Node.js SDK and Voucherify.js. See Migration Guide to see what is changed.

### Patch Changes

- [`7c491eb`](https://github.com/voucherifyio/voucherify-js-sdk/commit/7c491eb9a3a786e044a7f5e31c1a1529157d69e8) [#19](https://github.com/voucherifyio/voucherify-js-sdk/pull/19) Thanks [@pannga](https://github.com/pannga)! - Distributions types

  - Used FixMe convention for unknown types
  - Added Distributions types
  - Removed deprecated method
  - Updated Distribution types

* [`29f69e1`](https://github.com/voucherifyio/voucherify-js-sdk/commit/29f69e1a499c1576058e915bd683812b6c7a363c) [#28](https://github.com/voucherifyio/voucherify-js-sdk/pull/28) Thanks [@pannga](https://github.com/pannga)! - Added Rewards types

- [`dec48a0`](https://github.com/voucherifyio/voucherify-js-sdk/commit/dec48a08f5d3b2907a9533c95e3e15f3d2c10dd4) [#20](https://github.com/voucherifyio/voucherify-js-sdk/pull/20) Thanks [@pannga](https://github.com/pannga)! - Added Campaigns types

* [`4d01aad`](https://github.com/voucherifyio/voucherify-js-sdk/commit/4d01aad667312797c83e027d0d871afaeb7e4d12) [#18](https://github.com/voucherifyio/voucherify-js-sdk/pull/18) Thanks [@pannga](https://github.com/pannga)! - Updated Consents types

- [`0098874`](https://github.com/voucherifyio/voucherify-js-sdk/commit/0098874bb15c1b902fdb5f4ecff19d72beec0596) [#15](https://github.com/voucherifyio/voucherify-js-sdk/pull/15) Thanks [@pannga](https://github.com/pannga)! - Added ClientSide types

* [`1dec176`](https://github.com/voucherifyio/voucherify-js-sdk/commit/1dec176817f2d1b5e6a5c959f0cbca3c7ae63a6b) [#30](https://github.com/voucherifyio/voucherify-js-sdk/pull/30) Thanks [@pannga](https://github.com/pannga)! - Added Validation Rules types

- [`0098874`](https://github.com/voucherifyio/voucherify-js-sdk/commit/0098874bb15c1b902fdb5f4ecff19d72beec0596) [#15](https://github.com/voucherifyio/voucherify-js-sdk/pull/15) Thanks [@pannga](https://github.com/pannga)! - Updated types for client side publish method

* [`dec48a0`](https://github.com/voucherifyio/voucherify-js-sdk/commit/dec48a08f5d3b2907a9533c95e3e15f3d2c10dd4) [#20](https://github.com/voucherifyio/voucherify-js-sdk/pull/20) Thanks [@pannga](https://github.com/pannga)! - added missing method for publishing a ceratin voucher to selected campaign

- [`18bd006`](https://github.com/voucherifyio/voucherify-js-sdk/commit/18bd0061268a44b4cf00f431d55913df8b7087ce) [#25](https://github.com/voucherifyio/voucherify-js-sdk/pull/25) Thanks [@pannga](https://github.com/pannga)! - Added Promotions types

* [`3276101`](https://github.com/voucherifyio/voucherify-js-sdk/commit/32761019b9653ea00c9af8cd76b20e8736779ddf) [#29](https://github.com/voucherifyio/voucherify-js-sdk/pull/29) Thanks [@pannga](https://github.com/pannga)! - Added Segments types & missing Segment List method

- [`93adf99`](https://github.com/voucherifyio/voucherify-js-sdk/commit/93adf99c55cc43c09e0deaf8fae025676ac3b0a7) [#23](https://github.com/voucherifyio/voucherify-js-sdk/pull/23) Thanks [@pannga](https://github.com/pannga)! - Added Orders types

* [`c27f5b2`](https://github.com/voucherifyio/voucherify-js-sdk/commit/c27f5b28651602afc5800f71bba83c9aaf7bc7fe) [#24](https://github.com/voucherifyio/voucherify-js-sdk/pull/24) Thanks [@pannga](https://github.com/pannga)! - Added Products types

- [`2321908`](https://github.com/voucherifyio/voucherify-js-sdk/commit/2321908bf2f72ad696bc97e0ceff4d34c10f106d) [#31](https://github.com/voucherifyio/voucherify-js-sdk/pull/31) Thanks [@pannga](https://github.com/pannga)! - Added Validation types

* [`0098874`](https://github.com/voucherifyio/voucherify-js-sdk/commit/0098874bb15c1b902fdb5f4ecff19d72beec0596) [#15](https://github.com/voucherifyio/voucherify-js-sdk/pull/15) Thanks [@pannga](https://github.com/pannga)! - Used FixMe convention for unknown types

- [`e90cdec`](https://github.com/voucherifyio/voucherify-js-sdk/commit/e90cdec6a6d0f786d3a9cc5bbe7649ea5d2eec46) [#33](https://github.com/voucherifyio/voucherify-js-sdk/pull/33) Thanks [@pannga](https://github.com/pannga)! - Added Vouchers types

* [`4d01aad`](https://github.com/voucherifyio/voucherify-js-sdk/commit/4d01aad667312797c83e027d0d871afaeb7e4d12) [#18](https://github.com/voucherifyio/voucherify-js-sdk/pull/18) Thanks [@pannga](https://github.com/pannga)! - Added Consents type

- [`8628825`](https://github.com/voucherifyio/voucherify-js-sdk/commit/8628825df7e5a2ddfd746923277d162abd4ca516) [#27](https://github.com/voucherifyio/voucherify-js-sdk/pull/27) Thanks [@pannga](https://github.com/pannga)! - Added Redemptions types

* [`0098874`](https://github.com/voucherifyio/voucherify-js-sdk/commit/0098874bb15c1b902fdb5f4ecff19d72beec0596) [#15](https://github.com/voucherifyio/voucherify-js-sdk/pull/15) Thanks [@pannga](https://github.com/pannga)! - Added missing ClientSide types

- [`022b037`](https://github.com/voucherifyio/voucherify-js-sdk/commit/022b03753898801b083f45e6633a5ed97d22c2f6) [#17](https://github.com/voucherifyio/voucherify-js-sdk/pull/17) Thanks [@pannga](https://github.com/pannga)! - Added Events types

* [`022b037`](https://github.com/voucherifyio/voucherify-js-sdk/commit/022b03753898801b083f45e6633a5ed97d22c2f6) [#17](https://github.com/voucherifyio/voucherify-js-sdk/pull/17) Thanks [@pannga](https://github.com/pannga)! - Updated Events types

- [`920b5dd`](https://github.com/voucherifyio/voucherify-js-sdk/commit/920b5dd1c95bc7b3b3b85b60d4b8aa7ebbddcaa9) [#26](https://github.com/voucherifyio/voucherify-js-sdk/pull/26) Thanks [@pannga](https://github.com/pannga)! - Added Promotion Tiers types

* [`ed1de95`](https://github.com/voucherifyio/voucherify-js-sdk/commit/ed1de95e84282971c6f3fcc0875e67d2962194b6) [#21](https://github.com/voucherifyio/voucherify-js-sdk/pull/21) Thanks [@pannga](https://github.com/pannga)! - Added Loyalties types

- [`20752b9`](https://github.com/voucherifyio/voucherify-js-sdk/commit/20752b921f824c8bbbfc4b7197b0b87612eb760d) [#22](https://github.com/voucherifyio/voucherify-js-sdk/pull/22) Thanks [@pannga](https://github.com/pannga)! - Added Exports types

## 0.0.5

### Patch Changes

- [`1036e5d`](https://github.com/voucherifyio/voucherify-js-sdk/commit/1036e5d7507421faf4bea80bfe6bab9cf6a5f0b3) [#12](https://github.com/voucherifyio/voucherify-js-sdk/pull/12) Thanks [@eddyw](https://github.com/eddyw)! - Generate UMD bundle

## 0.0.4

### Patch Changes

- [`e3285c5`](https://github.com/voucherifyio/voucherify-js-sdk/commit/e3285c5c2f20d65a4b767c3d9eebdef9172259a1) [#10](https://github.com/voucherifyio/voucherify-js-sdk/pull/10) Thanks [@eddyw](https://github.com/eddyw)! - Export missing types

  - export missing type `CustomerRequest`
  - export missing type `CustomersCommonListRequest`

## 0.0.3

### Patch Changes

- [`ca8e470`](https://github.com/voucherifyio/voucherify-js-sdk/commit/ca8e470c1cb5bfb33d642069f40f3315d89b89d2) [#6](https://github.com/voucherifyio/voucherify-js-sdk/pull/6) Thanks [@eddyw](https://github.com/eddyw)! - - Add JSDoc comments to all namespaces with links to https://docs.voucherify.io/
  - setup typedoc to generate automatic documentation

## 0.0.2

### Patch Changes

- [`8e49408`](https://github.com/voucherifyio/voucherify-js-sdk/commit/8e494083837e8e932c26b3cad08479f4015ec2fc) [#5](https://github.com/voucherifyio/voucherify-js-sdk/pull/5) Thanks [@eddyw](https://github.com/eddyw)! - First SDK release
