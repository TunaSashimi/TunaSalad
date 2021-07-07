# TunaSalad

[![Release Version](https://img.shields.io/github/v/release/TunaSashimi/TunaSalad.svg)](https://github.com/TunaSashimi/TunaSalad/releases)
[![Code Size](https://img.shields.io/github/languages/code-size/TunaSashimi/TunaSalad)](https://github.com/TunaSashimi/TunaSalad)
[![Last Commit](https://img.shields.io/github/last-commit/TunaSashimi/TunaSalad)](https://github.com/TunaSashimi/TunaSalad/commits)
[![license](https://img.shields.io/github/license/TunaSashimi/TunaSushi)](https://github.com/TunaSashimi/TunaSalad/blob/master/LICENSE)

## Getting started

Step 1. Add the JitPack repository to your build file

To get a Git project into your build:
Add it in your root build.gradle at the end of repositories:

```gradle
	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```  
Step 2. Add the dependency
  
```gradle
  	dependencies {
	        implementation 'com.github.TunaSashimi:TunaSalad:1.0.01'
	}
```
	
## Known Issues

If the attributes defined in the TunaSalad library and the attributes defined in other libraries have the same name and different types, compilation errors will occur.The solution is to define an attribute with the same name in the attr of the main project, but the type contains both.

For example, The content attribute in TView in the TunaSalad library is string, and the content attribute in the constraintlayout library is reference.

When the types of attributes with the same name are inconsistent, you can configure a single content in the project, and the attribute is the union of the two.such as below.

```java
	<attr name="content" format="reference|string" />
```

## License
TunaSushi is under the MIT license. See the [LICENSE](https://github.com/TunaSashimi/TunaSalad/blob/master/LICENSE) file for details.
