## Modal

###### Dynamic classes
```
body: 			cd-hide-overflow
cd-modal-wrapper: 	cd-modal-open
```

###### Modal Structure
```
<div class="cd-modal-wrapper">
	<div class="cd-modal">
		content
	</div>
</div>
```

#### Open Modal:
- Add class `cd-modal-open` next to wrapper class `cd-modal-wrapper`.
- To hide body tag scroll, add class `cd-hide-overflow`.

#### Close Modal:
- Remove class `cd-modal-open` next to wrapper class `cd-modal-wrapper`.
- To show body tag scroll, remove class `cd-hide-overflow`.