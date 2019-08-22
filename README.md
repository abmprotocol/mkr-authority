# mkr-authority
Custom authority for allowing MKR to govern MKR.

Intentionally simple. Once set as the MKR token's authority, if the MKR token's `owner` field is subsequently set to
zero, the following properties obtain:
* any user may call MKR's `burn` function
* only authorized users (according to the MkrAuthority's `ward`s) can call MKR's `mint()` function
* only the `root` user set in the authority can call other `auth`-protected functions of the MKR contract

K proofs of the contract's functionality can be found in: https://github.com/makerdao/k-mkr-authority/
