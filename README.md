# About

Example project of writing JUnit tests using robolectric 0.13.+ on gradle build 0.13.2 and Android Studio 0.8.14

# Getting Started

## Import Project

* Clone project using git
* import project into Android Studio


## Running Tests

To run tests use the gradlew in the root of you project with the clean and test goals. 

	./gradlew clean test

Should end with output like below

	Executing test for {testThatSucceeds} with result: SUCCESS
	Executing test for {testThatFails} with result: FAILURE
	                                                  
	android.hcpl.be.mytestedapplication.MainActivityTest > testThatFails FAILED
	    java.lang.AssertionError at MainActivityTest.java:21
	                                                             
	2 tests completed, 1 failed                                  
	There were failing tests. See the report at: file:///Users/hcpl/Development/git/MyTestedApplication/app/build/test-report/debug/index.html
	:app:test                      
	               
	BUILD SUCCESSFUL

# Notes

I created a sample project using the Android Studio wizard. 

Next I followed the steps at https://github.com/robolectric/robolectric-gradle-plugin to configure everything for the junit tests. The only difference is that I had to add the junit dependency using 

	androidTestCompile 'junit:junit:4.10'

# Resources

* https://github.com/robolectric/robolectric-gradle-plugin


