# mta_multi
Multi-Target Application for Multi-Tenant Use-Case
```
mta --build-target CF --mtar target/mta_multi-CF.mtar buils
cf deploy target/mta_multi-CF.mtar
```
Deploy
```
cf env multi-nodejs | grep xsappname
vi mt_config/config.json
cf cs saas-registry application multi-app-saas-registry -c mt_config/config.json
cf bs multi-nodejs multi-app-saas-registry
cf restage multi-nodejs
```
