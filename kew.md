 
AngularJS extends HTML with ng-directives.
	The ng-app directive defines an AngularJS application.
	The ng-model directive binds the value of HTML controls (input, select, textarea) to application data.
	The ng-bind directive binds application data to the HTML view.

	v1
		<div ng-app="">
		  <p>Name: <input type="text" ng-model="name"></p>
		  <p ng-bind="name"></p>
		</div>
	v2
		<div ng-app="">
		  <p>Name: <input type="text" ng-model="name"></p>
		  <p>{{name}}</p>
		</div>

As you have already seen, AngularJS directives are HTML attributes with an ng prefix.
	The ng-init directive initializes AngularJS application variables.
	Example:
		<div ng-app="" ng-init="firstName='John'">
			<p>The name is <span ng-bind="firstName"></span></p>
		</div>

AngularJS expressions are written inside double braces: {{ expression }}.
	<p>My first expression: {{ 5 + 5 }}</p>

AngularJS Module
	var app = angular.module('myApp', []);
AngularJS Controller
	app.controller('myCtrl', function($scope) {
    $scope.firstName= "John";
    $scope.lastName= "Doe";
});
		<div ng-app="myApp" ng-controller="myCtrl">First Name:
			<input type="text" ng-model="firstName">
			<br>Last Name:
			<input type="text" ng-model="lastName">
			<br>
			<br>Full Name: {{firstName + " " + lastName}}</div>
		<script>
			var app = angular.module('myApp', []);
			app.controller('myCtrl', function($scope) {
			    $scope.firstName= "John";
			    $scope.lastName= "Doe";
			});
		</script>

AngularJS Numbers
	AngularJS numbers are like JavaScript numbers:
	Example:
		<div ng-app="" ng-init="quantity=1;cost=5">
			<p>Total in dollar: {{ quantity * cost }}</p>
		</div>

	Same example using ng-bind:
		Example:
			<div ng-app="" ng-init="quantity=1;cost=5">
				<p>Total in dollar: <span ng-bind="quantity * cost"></span></p>
			</div>

