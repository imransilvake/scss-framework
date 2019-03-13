# Navbar

## Positions
`cd-bottom-left` `cd-bottom-right` `cd-top-left` `cd-top-right` `cd-bottom` `cd-top`


## Structure
```
<nav class="cd-navigation-menu-wrapper">
	<ul class="cd-navigation-menu">
		<li><a href="#">Item 1</a></li>
		<li class="cd-dropdown cd-bottom-left|cd-bottom-right|cd-top-left|cd-top-right|cd-bottom|cd-top">
			<a href="#">Item 2 - Sub Menu</a>
			<ul>
				<li><a href="#">Item 1</a></li>
				<li><a href="#">Item 2</a></li>
				<li class="cd-dropdown cd-dropdown-sub">
					<a href="#">Item 3 - Sub Menu</a>
					<ul>
						<li><a href="#">Item 1</a></li>
						<li class="cd-dropdown cd-dropdown-sub">
							<a href="#">Item 2 - Sub Menu</a>
							<ul>
								<li><a href="#">Item 1</a></li>
								<li><a href="#">Item 2</a></li>
								<li><a href="#">Item 3</a></li>
								<li><a href="#">Item 4</a></li>
							</ul>
						</li>
						<li><a href="#">Item 3</a></li>
						<li><a href="#">Item 4</a></li>
					</ul>
				</li>
				<li><a href="#">Item 4</a></li>
			</ul>
		</li>

		<li><a href="#">Item 3</a></li>
		<li><a href="#">Item 4</a></li>
	</ul>
</nav>
```
