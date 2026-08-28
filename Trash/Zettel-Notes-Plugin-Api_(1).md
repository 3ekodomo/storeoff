├── app/ (2300 tokens)
    ├── .gitignore
    ├── jitpack.yml
    ├── consumer-rules.pro
    ├── src/ (1300 tokens)
    │   └── main/ (1300 tokens)
    │   │   ├── AndroidManifest.xml
    │   │   └── java/ (1200 tokens)
    │   │       └── org/ (1200 tokens)
    │   │           └── eu/ (1200 tokens)
    │   │               └── thedoc/ (1200 tokens)
    │   │                   └── zettelnotes/ (1200 tokens)
    │   │                       ├── interfaces/ (600 tokens)
    │   │                           ├── ScanInterface.java (200 tokens)
    │   │                           └── ButtonInterface.java (400 tokens)
    │   │                       └── broadcasts/ (600 tokens)
    │   │                           └── AbstractPluginReceiver.java (600 tokens)
    └── build.gradle (800 tokens)
├── gradle/ (200 tokens)
    └── wrapper/ (200 tokens)
    │   ├── gradle-wrapper.jar
    │   └── gradle-wrapper.properties
├── .gitignore
├── README.md
├── settings.gradle
├── LICENSE (300 tokens)
├── gradle.properties (300 tokens)
├── gradlew.bat (700 tokens)
└── gradlew (1400 tokens)


/app/.gitignore:
--------------------------------------------------------------------------------
1 | /build


--------------------------------------------------------------------------------
/app/jitpack.yml:
--------------------------------------------------------------------------------
1 | jdk:
2 |   - openjdk17
3 | before_install:
4 |   - ./scripts/prepareJitpackEnvironment.sh


--------------------------------------------------------------------------------
/gradle/wrapper/gradle-wrapper.jar:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/damionx7/Zettel-Notes-Plugin-Api/HEAD/gradle/wrapper/gradle-wrapper.jar


--------------------------------------------------------------------------------
/.gitignore:
--------------------------------------------------------------------------------
 1 | *.iml
 2 | .gradle
 3 | /local.properties
 4 | .DS_Store
 5 | /build
 6 | /captures
 7 | .externalNativeBuild
 8 | .cxx
 9 | local.properties
10 | github.properties
11 | /app/build
12 | /release
13 | .idea
14 | 
15 | 


--------------------------------------------------------------------------------
/app/consumer-rules.pro:
--------------------------------------------------------------------------------
1 | # Exclude Interface From Proguard
2 | -keep class org.eu.thedoc.zettelnotes.interfaces.** { *; }
3 | -keepclassmembers class org.eu.thedoc.zettelnotes.interfaces.** {
4 |     <fields>;
5 |     <init>();
6 |     <methods>;
7 | }


--------------------------------------------------------------------------------
/README.md:
--------------------------------------------------------------------------------
1 | # Zettel-Notes-Plugin-Api
2 | 
3 | Plugin interface for Zettel Notes : Markdown Note Taking app for Android https://thedoc.eu.org/zettel-notes/
4 | 
5 | For implementation see other plugin examples: https://github.com/damionx7/Zettel-Notes-Plugin-Buttons/
6 | 


--------------------------------------------------------------------------------
/gradle/wrapper/gradle-wrapper.properties:
--------------------------------------------------------------------------------
1 | #Thu May 11 17:30:26 IST 2023
2 | distributionBase=GRADLE_USER_HOME
3 | distributionPath=wrapper/dists
4 | distributionUrl=https\://services.gradle.org/distributions/gradle-8.14.1-bin.zip
5 | zipStoreBase=GRADLE_USER_HOME
6 | zipStorePath=wrapper/dists


--------------------------------------------------------------------------------
/settings.gradle:
--------------------------------------------------------------------------------
 1 | pluginManagement {
 2 |     repositories {
 3 |         google()
 4 |         mavenCentral()
 5 |     }
 6 | }
 7 | dependencyResolutionManagement {
 8 |     repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
 9 |     repositories {
10 |         google()
11 |         mavenCentral()
12 |     }
13 | }
14 | 
15 | rootProject.name = "Zettel Notes Plugin Base"
16 | include ':app'
17 | 


--------------------------------------------------------------------------------
/app/src/main/AndroidManifest.xml:
--------------------------------------------------------------------------------
 1 | <?xml version="1.0" encoding="utf-8"?>
 2 | <manifest xmlns:android="http://schemas.android.com/apk/res/android">
 3 | 
 4 |     <application>
 5 |         <meta-data
 6 |            android:name="@string/plugin_button_metadata_api_string"
 7 |            android:value="@string/button_api_version" />
 8 |         <meta-data
 9 |            android:name="@string/plugin_scan_metadata_api_string"
10 |            android:value="@string/scan_api_version" />
11 |     </application>
12 | 
13 | </manifest>


--------------------------------------------------------------------------------
/app/src/main/java/org/eu/thedoc/zettelnotes/interfaces/ScanInterface.java:
--------------------------------------------------------------------------------
 1 | package org.eu.thedoc.zettelnotes.interfaces;
 2 | 
 3 | import android.content.Context;
 4 | import java.util.List;
 5 | 
 6 | public abstract class ScanInterface {
 7 | 
 8 |   public abstract String getName();
 9 | 
10 |   public abstract Listener getListener();
11 | 
12 |   public interface Listener {
13 | 
14 |     boolean onScanText(Context context, String category, String fileUri, String fileTitle, String text);
15 | 
16 |     String onProcessText(Context context, String text);
17 | 
18 |     void onDeleteUris(Context context, String category, List<String> fileUris);
19 |   }
20 | 
21 | }


--------------------------------------------------------------------------------
/LICENSE:
--------------------------------------------------------------------------------
 1 | MIT License
 2 | 
 3 | Copyright (c) 2021 Rohit
 4 | 
 5 | Permission is hereby granted, free of charge, to any person obtaining a copy
 6 | of this software and associated documentation files (the "Software"), to deal
 7 | in the Software without restriction, including without limitation the rights
 8 | to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
 9 | copies of the Software, and to permit persons to whom the Software is
10 | furnished to do so, subject to the following conditions:
11 | 
12 | The above copyright notice and this permission notice shall be included in all
13 | copies or substantial portions of the Software.
14 | 
15 | THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
16 | IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
17 | FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
18 | AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
19 | LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
20 | OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
21 | SOFTWARE.
22 | 


--------------------------------------------------------------------------------
/gradle.properties:
--------------------------------------------------------------------------------
 1 | # Project-wide Gradle settings.
 2 | # IDE (e.g. Android Studio) users:
 3 | # Gradle settings configured through the IDE *will override*
 4 | # any settings specified in this file.
 5 | # For more details on how to configure your build environment visit
 6 | # http://www.gradle.org/docs/current/userguide/build_environment.html
 7 | # Specifies the JVM arguments used for the daemon process.
 8 | # The setting is particularly useful for tweaking memory settings.
 9 | org.gradle.jvmargs=-Xmx2048m -Dfile.encoding=UTF-8
10 | # When configured, Gradle will run in incubating parallel mode.
11 | # This option should only be used with decoupled projects. More details, visit
12 | # http://www.gradle.org/docs/current/userguide/multi_project_builds.html#sec:decoupled_projects
13 | # org.gradle.parallel=true
14 | # AndroidX package structure to make it clearer which packages are bundled with the
15 | # Android operating system, and which are packaged with your app"s APK
16 | # https://developer.android.com/topic/libraries/support-library/androidx-rn
17 | android.useAndroidX=true
18 | android.nonTransitiveRClass=false
19 | android.nonFinalResIds=false
20 | org.gradle.configuration-cache=true


--------------------------------------------------------------------------------
/app/src/main/java/org/eu/thedoc/zettelnotes/interfaces/ButtonInterface.java:
--------------------------------------------------------------------------------
 1 | package org.eu.thedoc.zettelnotes.interfaces;
 2 | 
 3 | import android.content.Intent;
 4 | import android.net.Uri;
 5 | import android.util.Pair;
 6 | import androidx.activity.result.ActivityResult;
 7 | 
 8 | public abstract class ButtonInterface {
 9 | 
10 |   protected Callback mCallback;
11 | 
12 |   public abstract String getName();
13 | 
14 |   public abstract Listener getListener();
15 | 
16 |   public void registerCallback(Callback callback) {
17 |     mCallback = callback;
18 |   }
19 | 
20 |   public interface Listener {
21 | 
22 |     void onClick();
23 | 
24 |     boolean onLongClick();
25 |   }
26 | 
27 |   public interface ActivityResultListener {
28 | 
29 |     void getActivityResult(ActivityResult result);
30 |   }
31 | 
32 |   public interface Callback {
33 | 
34 |     void startActivityForResult(Intent intent);
35 | 
36 |     void setActivityResultListener(ActivityResultListener result);
37 | 
38 |     void insertText(String text);
39 | 
40 |     void replaceTextSelected(String text);
41 | 
42 |     /***
43 |      * @return Pair with 1st Integer as line start index
44 |      * and String as line content
45 |      */
46 |     Pair<Integer, String> getCurrentLine();
47 | 
48 |     /***
49 |      * Replaces text in line at line start index
50 |      * with Text in Pair
51 |      */
52 |     void replaceCurrentLine(Pair<Integer, String> pair);
53 | 
54 |     String getTextSelected(boolean returnAllIfEmpty);
55 | 
56 |     void insertUri(Uri uri);
57 |   }
58 | 
59 | }
60 | 


--------------------------------------------------------------------------------
/app/src/main/java/org/eu/thedoc/zettelnotes/broadcasts/AbstractPluginReceiver.java:
--------------------------------------------------------------------------------
 1 | package org.eu.thedoc.zettelnotes.broadcasts;
 2 | 
 3 | import android.content.Intent;
 4 | import org.eu.thedoc.zettelnotes.interfaces.BuildConfig;
 5 | 
 6 | public class AbstractPluginReceiver {
 7 | 
 8 |   //note uri
 9 |   public static final String EXTRAS_URI = "arg-uri";
10 |   //repository
11 |   public static final String EXTRAS_REPOSITORY = "arg-repository";
12 |   //start with edit mode
13 |   public static final String EXTRAS_EDIT = "arg-edit";
14 |   //line number in note
15 |   public static final String EXTRAS_LINE_INDEXES = "arg-line-indexes";
16 |   //replacement of the line
17 |   public static final String EXTRAS_REPLACEMENT = "arg-replacement-text";
18 | 
19 |   //intent action to open file uri
20 |   public static final String INTENT_ACTION_PLUGIN_OPEN_URI = "org.eu.thedoc.zettelnotes.broadcast.plugins.OPEN_URI";
21 |   //intent action to open and replace specific line in file uri
22 |   public static final String INTENT_ACTION_PLUGIN_OPEN_AND_REPLACE_URI = "org.eu.thedoc.zettelnotes.broadcast.plugins.OPEN_AND_REPLACE_URI";
23 | 
24 |   public static class IntentBuilder {
25 | 
26 |     private final Intent intent;
27 | 
28 |     private IntentBuilder() {
29 |       intent = new Intent();
30 |       intent.setPackage(BuildConfig.ZETTEL_PACKAGE_NAME);
31 |     }
32 | 
33 |     public static IntentBuilder getInstance() {
34 |       return new IntentBuilder();
35 |     }
36 | 
37 |     public IntentBuilder setActionOpenUri() {
38 |       intent.setAction(INTENT_ACTION_PLUGIN_OPEN_URI);
39 |       return this;
40 |     }
41 | 
42 |     public IntentBuilder setDebug() {
43 |       intent.setPackage(BuildConfig.ZETTEL_PACKAGE_NAME_DEBUG);
44 |       return this;
45 |     }
46 | 
47 |     public IntentBuilder setActionOpenAndReplace(String text) {
48 |       intent.setAction(INTENT_ACTION_PLUGIN_OPEN_AND_REPLACE_URI);
49 |       intent.putExtra(EXTRAS_REPLACEMENT, text);
50 |       return this;
51 |     }
52 | 
53 |     public IntentBuilder setLineIndexes(int[] indexes) {
54 |       intent.putExtra(EXTRAS_LINE_INDEXES, indexes);
55 |       return this;
56 |     }
57 | 
58 |     public IntentBuilder setUri(String uri) {
59 |       intent.putExtra(EXTRAS_URI, uri);
60 |       return this;
61 |     }
62 | 
63 |     public IntentBuilder setRepository(String repository) {
64 |       intent.putExtra(EXTRAS_REPOSITORY, repository);
65 |       return this;
66 |     }
67 | 
68 |     public IntentBuilder setEdit(boolean edit) {
69 |       intent.putExtra(EXTRAS_EDIT, edit);
70 |       return this;
71 |     }
72 | 
73 |     public Intent build() {
74 |       return intent;
75 |     }
76 |   }
77 | 
78 | }
79 | 


--------------------------------------------------------------------------------
/gradlew.bat:
--------------------------------------------------------------------------------
 1 | @rem
 2 | @rem Copyright 2015 the original author or authors.
 3 | @rem
 4 | @rem Licensed under the Apache License, Version 2.0 (the "License");
 5 | @rem you may not use this file except in compliance with the License.
 6 | @rem You may obtain a copy of the License at
 7 | @rem
 8 | @rem      https://www.apache.org/licenses/LICENSE-2.0
 9 | @rem
10 | @rem Unless required by applicable law or agreed to in writing, software
11 | @rem distributed under the License is distributed on an "AS IS" BASIS,
12 | @rem WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
13 | @rem See the License for the specific language governing permissions and
14 | @rem limitations under the License.
15 | @rem
16 | 
17 | @if "%DEBUG%" == "" @echo off
18 | @rem ##########################################################################
19 | @rem
20 | @rem  Gradle startup script for Windows
21 | @rem
22 | @rem ##########################################################################
23 | 
24 | @rem Set local scope for the variables with windows NT shell
25 | if "%OS%"=="Windows_NT" setlocal
26 | 
27 | set DIRNAME=%~dp0
28 | if "%DIRNAME%" == "" set DIRNAME=.
29 | set APP_BASE_NAME=%~n0
30 | set APP_HOME=%DIRNAME%
31 | 
32 | @rem Resolve any "." and ".." in APP_HOME to make it shorter.
33 | for %%i in ("%APP_HOME%") do set APP_HOME=%%~fi
34 | 
35 | @rem Add default JVM options here. You can also use JAVA_OPTS and GRADLE_OPTS to pass JVM options to this script.
36 | set DEFAULT_JVM_OPTS="-Xmx64m" "-Xms64m"
37 | 
38 | @rem Find java.exe
39 | if defined JAVA_HOME goto findJavaFromJavaHome
40 | 
41 | set JAVA_EXE=java.exe
42 | %JAVA_EXE% -version >NUL 2>&1
43 | if "%ERRORLEVEL%" == "0" goto execute
44 | 
45 | echo.
46 | echo ERROR: JAVA_HOME is not set and no 'java' command could be found in your PATH.
47 | echo.
48 | echo Please set the JAVA_HOME variable in your environment to match the
49 | echo location of your Java installation.
50 | 
51 | goto fail
52 | 
53 | :findJavaFromJavaHome
54 | set JAVA_HOME=%JAVA_HOME:"=%
55 | set JAVA_EXE=%JAVA_HOME%/bin/java.exe
56 | 
57 | if exist "%JAVA_EXE%" goto execute
58 | 
59 | echo.
60 | echo ERROR: JAVA_HOME is set to an invalid directory: %JAVA_HOME%
61 | echo.
62 | echo Please set the JAVA_HOME variable in your environment to match the
63 | echo location of your Java installation.
64 | 
65 | goto fail
66 | 
67 | :execute
68 | @rem Setup the command line
69 | 
70 | set CLASSPATH=%APP_HOME%\gradle\wrapper\gradle-wrapper.jar
71 | 
72 | 
73 | @rem Execute Gradle
74 | "%JAVA_EXE%" %DEFAULT_JVM_OPTS% %JAVA_OPTS% %GRADLE_OPTS% "-Dorg.gradle.appname=%APP_BASE_NAME%" -classpath "%CLASSPATH%" org.gradle.wrapper.GradleWrapperMain %*
75 | 
76 | :end
77 | @rem End local scope for the variables with windows NT shell
78 | if "%ERRORLEVEL%"=="0" goto mainEnd
79 | 
80 | :fail
81 | rem Set variable GRADLE_EXIT_CONSOLE if you need the _script_ return code instead of
82 | rem the _cmd.exe /c_ return code!
83 | if  not "" == "%GRADLE_EXIT_CONSOLE%" exit 1
84 | exit /b 1
85 | 
86 | :mainEnd
87 | if "%OS%"=="Windows_NT" endlocal
88 | 
89 | :omega
90 | 


--------------------------------------------------------------------------------
/app/build.gradle:
--------------------------------------------------------------------------------
 1 | plugins {
 2 |     id 'com.android.library'
 3 |     id 'maven-publish'
 4 | }
 5 | 
 6 | def appVersion = 28
 7 | 
 8 | def buttonApiVersion = 11
 9 | def buttonQueryIntent = "org.eu.thedoc.zettelnotes.intent.buttons"
10 | def buttonMetadataApiVersionString = "org.eu.thedoc.zettelnotes.interfaces.version"
11 | 
12 | def scanApiVersion = 3
13 | def scanQueryIntent = "org.eu.thedoc.zettelnotes.intent.scan"
14 | def scanMetadataApiVersionString = "org.eu.thedoc.zettelnotes.interfaces.scan.version"
15 | 
16 | def zettelNotesPackageName = "org.eu.thedoc.zettelnotes"
17 | def zettelNotesPackageNameDebug = "org.eu.thedoc.zettelnotes.debug"
18 | 
19 | android {
20 |     namespace "org.eu.thedoc.zettelnotes.interfaces"
21 |     compileSdk 35
22 | 
23 |     defaultConfig {
24 |         minSdk 24
25 |         targetSdk 34
26 |         versionCode appVersion
27 |         versionName "${appVersion}"
28 |         //button interface
29 |         resValue "string", "button_api_version", "\"${buttonApiVersion}\""
30 |         buildConfigField("String", "BUTTON_API_VERSION", "\"${buttonApiVersion}\"")
31 |         resValue "string", "plugin_button_query_intent", "\"${buttonQueryIntent}\""
32 |         buildConfigField("String", "PLUGIN_BUTTON_QUERY_INTENT", "\"${buttonQueryIntent}\"")
33 |         resValue "string", "plugin_button_metadata_api_string", "\"${buttonMetadataApiVersionString}\""
34 |         buildConfigField("String", "PLUGIN_BUTTON_METADATA_API_STRING", "\"${buttonMetadataApiVersionString}\"")
35 |         //scan interface
36 |         resValue "string", "scan_api_version", "\"${scanApiVersion}\""
37 |         buildConfigField("String", "SCAN_API_VERSION", "\"${scanApiVersion}\"")
38 |         resValue "string", "plugin_scan_query_intent", "\"${scanQueryIntent}\""
39 |         buildConfigField("String", "PLUGIN_SCAN_QUERY_INTENT", "\"${scanQueryIntent}\"")
40 |         resValue "string", "plugin_scan_metadata_api_string", "\"${scanMetadataApiVersionString}\""
41 |         buildConfigField("String", "PLUGIN_SCAN_METADATA_API_STRING", "\"${scanMetadataApiVersionString}\"")
42 |         //package names needed for broadcast receiver
43 |         resValue "string", "zettel_package_name", "\"${zettelNotesPackageName}\""
44 |         resValue "string", "zettel_package_name_debug", "\"${zettelNotesPackageNameDebug}\""
45 |         buildConfigField "String", "ZETTEL_PACKAGE_NAME", "\"${zettelNotesPackageName}\""
46 |         buildConfigField "String", "ZETTEL_PACKAGE_NAME_DEBUG", "\"${zettelNotesPackageNameDebug}\""
47 | 
48 |         consumerProguardFiles "consumer-rules.pro"
49 |         testInstrumentationRunner "androidx.test.runner.AndroidJUnitRunner"
50 |     }
51 | 
52 |     compileOptions {
53 |         sourceCompatibility JavaVersion.VERSION_17
54 |         targetCompatibility JavaVersion.VERSION_17
55 |     }
56 | 
57 |     publishing {
58 |         multipleVariants {
59 |             includeBuildTypeValues('release')
60 |         }
61 |     }
62 |     buildFeatures {
63 |         buildConfig true
64 |     }
65 | 
66 | }
67 | 
68 | dependencies {
69 |     api "androidx.appcompat:appcompat:1.7.1"
70 | }
71 | 
72 | afterEvaluate {
73 |     publishing {
74 |         publications {
75 |             release(MavenPublication) {
76 |                 groupId = 'com.github.damionx7'
77 |                 artifactId = 'Zettel-Notes-Plugin-Api'
78 |                 version = "${appVersion}"
79 | 
80 |                 afterEvaluate {
81 |                     from components.default
82 |                 }
83 |             }
84 |         }
85 |     }
86 | }


--------------------------------------------------------------------------------
/gradlew:
--------------------------------------------------------------------------------
  1 | #!/usr/bin/env sh
  2 | 
  3 | #
  4 | # Copyright 2015 the original author or authors.
  5 | #
  6 | # Licensed under the Apache License, Version 2.0 (the "License");
  7 | # you may not use this file except in compliance with the License.
  8 | # You may obtain a copy of the License at
  9 | #
 10 | #      https://www.apache.org/licenses/LICENSE-2.0
 11 | #
 12 | # Unless required by applicable law or agreed to in writing, software
 13 | # distributed under the License is distributed on an "AS IS" BASIS,
 14 | # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 15 | # See the License for the specific language governing permissions and
 16 | # limitations under the License.
 17 | #
 18 | 
 19 | ##############################################################################
 20 | ##
 21 | ##  Gradle start up script for UN*X
 22 | ##
 23 | ##############################################################################
 24 | 
 25 | # Attempt to set APP_HOME
 26 | # Resolve links: $0 may be a link
 27 | PRG="$0"
 28 | # Need this for relative symlinks.
 29 | while [ -h "$PRG" ] ; do
 30 |     ls=`ls -ld "$PRG"`
 31 |     link=`expr "$ls" : '.*-> \(.*\)$'`
 32 |     if expr "$link" : '/.*' > /dev/null; then
 33 |         PRG="$link"
 34 |     else
 35 |         PRG=`dirname "$PRG"`"/$link"
 36 |     fi
 37 | done
 38 | SAVED="`pwd`"
 39 | cd "`dirname \"$PRG\"`/" >/dev/null
 40 | APP_HOME="`pwd -P`"
 41 | cd "$SAVED" >/dev/null
 42 | 
 43 | APP_NAME="Gradle"
 44 | APP_BASE_NAME=`basename "$0"`
 45 | 
 46 | # Add default JVM options here. You can also use JAVA_OPTS and GRADLE_OPTS to pass JVM options to this script.
 47 | DEFAULT_JVM_OPTS='"-Xmx64m" "-Xms64m"'
 48 | 
 49 | # Use the maximum available, or set MAX_FD != -1 to use that value.
 50 | MAX_FD="maximum"
 51 | 
 52 | warn () {
 53 |     echo "$*"
 54 | }
 55 | 
 56 | die () {
 57 |     echo
 58 |     echo "$*"
 59 |     echo
 60 |     exit 1
 61 | }
 62 | 
 63 | # OS specific support (must be 'true' or 'false').
 64 | cygwin=false
 65 | msys=false
 66 | darwin=false
 67 | nonstop=false
 68 | case "`uname`" in
 69 |   CYGWIN* )
 70 |     cygwin=true
 71 |     ;;
 72 |   Darwin* )
 73 |     darwin=true
 74 |     ;;
 75 |   MINGW* )
 76 |     msys=true
 77 |     ;;
 78 |   NONSTOP* )
 79 |     nonstop=true
 80 |     ;;
 81 | esac
 82 | 
 83 | CLASSPATH=$APP_HOME/gradle/wrapper/gradle-wrapper.jar
 84 | 
 85 | 
 86 | # Determine the Java command to use to start the JVM.
 87 | if [ -n "$JAVA_HOME" ] ; then
 88 |     if [ -x "$JAVA_HOME/jre/sh/java" ] ; then
 89 |         # IBM's JDK on AIX uses strange locations for the executables
 90 |         JAVACMD="$JAVA_HOME/jre/sh/java"
 91 |     else
 92 |         JAVACMD="$JAVA_HOME/bin/java"
 93 |     fi
 94 |     if [ ! -x "$JAVACMD" ] ; then
 95 |         die "ERROR: JAVA_HOME is set to an invalid directory: $JAVA_HOME
 96 | 
 97 | Please set the JAVA_HOME variable in your environment to match the
 98 | location of your Java installation."
 99 |     fi
100 | else
101 |     JAVACMD="java"
102 |     which java >/dev/null 2>&1 || die "ERROR: JAVA_HOME is not set and no 'java' command could be found in your PATH.
103 | 
104 | Please set the JAVA_HOME variable in your environment to match the
105 | location of your Java installation."
106 | fi
107 | 
108 | # Increase the maximum file descriptors if we can.
109 | if [ "$cygwin" = "false" -a "$darwin" = "false" -a "$nonstop" = "false" ] ; then
110 |     MAX_FD_LIMIT=`ulimit -H -n`
111 |     if [ $? -eq 0 ] ; then
112 |         if [ "$MAX_FD" = "maximum" -o "$MAX_FD" = "max" ] ; then
113 |             MAX_FD="$MAX_FD_LIMIT"
114 |         fi
115 |         ulimit -n $MAX_FD
116 |         if [ $? -ne 0 ] ; then
117 |             warn "Could not set maximum file descriptor limit: $MAX_FD"
118 |         fi
119 |     else
120 |         warn "Could not query maximum file descriptor limit: $MAX_FD_LIMIT"
121 |     fi
122 | fi
123 | 
124 | # For Darwin, add options to specify how the application appears in the dock
125 | if $darwin; then
126 |     GRADLE_OPTS="$GRADLE_OPTS \"-Xdock:name=$APP_NAME\" \"-Xdock:icon=$APP_HOME/media/gradle.icns\""
127 | fi
128 | 
129 | # For Cygwin or MSYS, switch paths to Windows format before running java
130 | if [ "$cygwin" = "true" -o "$msys" = "true" ] ; then
131 |     APP_HOME=`cygpath --path --mixed "$APP_HOME"`
132 |     CLASSPATH=`cygpath --path --mixed "$CLASSPATH"`
133 | 
134 |     JAVACMD=`cygpath --unix "$JAVACMD"`
135 | 
136 |     # We build the pattern for arguments to be converted via cygpath
137 |     ROOTDIRSRAW=`find -L / -maxdepth 1 -mindepth 1 -type d 2>/dev/null`
138 |     SEP=""
139 |     for dir in $ROOTDIRSRAW ; do
140 |         ROOTDIRS="$ROOTDIRS$SEP$dir"
141 |         SEP="|"
142 |     done
143 |     OURCYGPATTERN="(^($ROOTDIRS))"
144 |     # Add a user-defined pattern to the cygpath arguments
145 |     if [ "$GRADLE_CYGPATTERN" != "" ] ; then
146 |         OURCYGPATTERN="$OURCYGPATTERN|($GRADLE_CYGPATTERN)"
147 |     fi
148 |     # Now convert the arguments - kludge to limit ourselves to /bin/sh
149 |     i=0
150 |     for arg in "$@" ; do
151 |         CHECK=`echo "$arg"|egrep -c "$OURCYGPATTERN" -`
152 |         CHECK2=`echo "$arg"|egrep -c "^-"`                                 ### Determine if an option
153 | 
154 |         if [ $CHECK -ne 0 ] && [ $CHECK2 -eq 0 ] ; then                    ### Added a condition
155 |             eval `echo args$i`=`cygpath --path --ignore --mixed "$arg"`
156 |         else
157 |             eval `echo args$i`="\"$arg\""
158 |         fi
159 |         i=`expr $i + 1`
160 |     done
161 |     case $i in
162 |         0) set -- ;;
163 |         1) set -- "$args0" ;;
164 |         2) set -- "$args0" "$args1" ;;
165 |         3) set -- "$args0" "$args1" "$args2" ;;
166 |         4) set -- "$args0" "$args1" "$args2" "$args3" ;;
167 |         5) set -- "$args0" "$args1" "$args2" "$args3" "$args4" ;;
168 |         6) set -- "$args0" "$args1" "$args2" "$args3" "$args4" "$args5" ;;
169 |         7) set -- "$args0" "$args1" "$args2" "$args3" "$args4" "$args5" "$args6" ;;
170 |         8) set -- "$args0" "$args1" "$args2" "$args3" "$args4" "$args5" "$args6" "$args7" ;;
171 |         9) set -- "$args0" "$args1" "$args2" "$args3" "$args4" "$args5" "$args6" "$args7" "$args8" ;;
172 |     esac
173 | fi
174 | 
175 | # Escape application args
176 | save () {
177 |     for i do printf %s\\n "$i" | sed "s/'/'\\\\''/g;1s/^/'/;\$s/\$/' \\\\/" ; done
178 |     echo " "
179 | }
180 | APP_ARGS=`save "$@"`
181 | 
182 | # Collect all arguments for the java command, following the shell quoting and substitution rules
183 | eval set -- $DEFAULT_JVM_OPTS $JAVA_OPTS $GRADLE_OPTS "\"-Dorg.gradle.appname=$APP_BASE_NAME\"" -classpath "\"$CLASSPATH\"" org.gradle.wrapper.GradleWrapperMain "$APP_ARGS"
184 | 
185 | exec "$JAVACMD" "$@"
186 | 


--------------------------------------------------------------------------------
