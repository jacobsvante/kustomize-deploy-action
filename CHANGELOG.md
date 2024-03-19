# Changelog

## [0.2.3](https://github.com/jacobsvante/kustomize-deploy-action/compare/v0.2.2...v0.2.3) (2024-03-19)


### Bug Fixes

* Missing base kustomization.yaml file wasn't properly supported ([397c5f9](https://github.com/jacobsvante/kustomize-deploy-action/commit/397c5f935be47b33b0d31527e045c47789e32183))

## [0.2.2](https://github.com/jacobsvante/kustomize-deploy-action/compare/v0.2.1...v0.2.2) (2024-03-19)


### Bug Fixes

* Don't parse non-existing kustomization-base-dir kustomization.yaml file ([2e1bb3d](https://github.com/jacobsvante/kustomize-deploy-action/commit/2e1bb3d3ecf0b889216efad32cac5dc635f70fdd))
* Upgrade to setup-kubectl v4 ([a41126f](https://github.com/jacobsvante/kustomize-deploy-action/commit/a41126fbd704b2370aaf1a3d42bcefcf374e26be))
* Use upstream yamler version again and disable multidoc ([936c371](https://github.com/jacobsvante/kustomize-deploy-action/commit/936c371ec987294de54124a1be39bb9663037f5e))

## [0.2.1](https://github.com/jacobsvante/kustomize-deploy-action/compare/v0.2.0...v0.2.1) (2023-01-12)


### Bug Fixes

* Remove deprecation messages from yamler ([2cfb874](https://github.com/jacobsvante/kustomize-deploy-action/commit/2cfb8749ef2c29c73f908226df11e110488f30e2))

## [0.2.0](https://github.com/jacobsvante/kustomize-deploy-action/compare/v0.1.1...v0.2.0) (2022-09-01)


### ⚠ BREAKING CHANGES

* Rename `image-tag` to `docker-tag`

### Features

* Don't require docker inputs ([2f45afa](https://github.com/jacobsvante/kustomize-deploy-action/commit/2f45afa42aa25d1e523ec13eda849ead729571ff))


### Bug Fixes

* Rename `image-tag` to `docker-tag` ([8b324bb](https://github.com/jacobsvante/kustomize-deploy-action/commit/8b324bb651ab5e0e31229859510f2c87fe733a4f))

## [0.1.1](https://github.com/jacobsvante/kustomize-deploy-action/compare/v0.1.0...v0.1.1) (2022-08-29)


### Bug Fixes

* github-release as separate workflow ([57abc1a](https://github.com/jacobsvante/kustomize-deploy-action/commit/57abc1acca3a4b4033c2a2038b4cae7be1e4a4ba))

## 0.1.0 (2022-08-29)


### Bug Fixes

* Initial commit ([58995cc](https://github.com/jacobsvante/kustomize-deploy-action/commit/58995cc0bcc20e58379a87f04c23ca1cddc66cc7))
