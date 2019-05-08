# XPermission
极简·仅一个类权限适配工具


Usage:
====
//Single Permission
```Java
XPermission.requestAllPermission(this, Collections.singletonList(
                Manifest.permission.WRITE_EXTERNAL_STORAGE
        ), new XPermission.PermissionSingleResult() {
            @Override
            protected void result(boolean accept) {
                if (accept) {
                    //Do something
                }else{

                }
            }
        });
```

//Multi Permission
```Java
XPermission.requestAllPermission(this, Arrays.asList(
                Manifest.permission.READ_PHONE_STATE,
                Manifest.permission.ACCESS_COARSE_LOCATION,
                Manifest.permission.CAMERA
        ), new XPermission.PermissionResult() {
            @Override
            public void Granted(String[] permission) {
                //Do something
            }

            @Override
            public void Denied(String[] permission) {
                //Do something
            }
        });
```