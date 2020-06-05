# boilerplate-demo

## Bootstrapping
```
mkdir -p boilerplate && \
curl https://raw.githubusercontent.com/dustman9000/boilerplate/master/boilerplate/update.sh -o boilerplate/update.sh && \
chmod +x boilerplate/update.sh
```

Create boilerplate/update.cfg with desired "conventions":
```
lyft/golang_test_targets
lyft/golang_support_tools
```

Makefile:
```
export REPOSITORY=boilerplate-demo
-include boilerplate/lyft/golang_test_targets/Makefile

.PHONY: update_boilerplate
update_boilerplate:
	@boilerplate/update.sh
```

Run update
```
make update_boilerplate
```
