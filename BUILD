# Copyright 2021 curoky(cccuroky@gmail.com).
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

cc_library(
    name = "folly",
    srcs = glob(
        ["folly/**/*.cpp"],
        exclude = [
            "folly/**/test/**",
            "folly/**/tests/**",
            "folly/**/example/**",
            "folly/**/examples/**",
            "folly/**/tool/**",
            "folly/**/tools/**",

            "folly/python/**",
            "folly/executors/**",
            "folly/ssl/**",
            "folly/folly/io/async/ssl/**",
            "folly/ext/**",
            "folly/experimental/exception_tracer/**",
            "folly/experimental/TestUtil.cpp",
            "folly/experimental/crypto/**",
            "folly/experimental/io/**",
            "folly/experimental/JSONSchemaTester.cpp",
            # add 2024
            "folly/experimental/**",
            "folly/futures/**",
            "folly/fibers/**",
            "folly/io/coro/**",
            "folly/experimental/observer/**",
            "folly/experimental/symbolizer/**",
            "folly/io/async/**",
            "folly/portability/OpenSSL.cpp",

        ],
    ),
    hdrs = glob(["folly/**/*.h"]),
    includes = ["."],
    copts = [
      "-g",
      "-ggdb",
      "-O0",
      "-fno-omit-frame-pointer",
      "-gno-statement-frontiers",
      "-gno-variable-location-views",
      "-Wno-deprecated-declarations",
      "-Wno-deprecated",
      "-Wno-sign-compare",
      "-Wno-unknown-pragmas",
      "-Wno-unused-but-set-variable",
      "-Wno-unused-function",
      "-Wno-unused-value",
      "-Wno-unused-variable",
      "-Wno-unused-local-typedefs",
      "-Wno-maybe-uninitialized",
      "-mavx",
      "-mavx2",
      "-mpclmul",
      "-msse2",
    ],
    linkopts = [
        "-ldl",
        "-lpthread",
    ],
    visibility = ["//visibility:public"],
    deps = [
        "@boost//:algorithm",
        "@boost//:container",
        "@boost//:context",
        "@boost//:crc",
        "@boost//:filesystem",
        "@boost//:function_types",
        "@boost//:functional",
        "@boost//:interprocess",
        "@boost//:intrusive",
        "@boost//:multi_index",
        "@boost//:operators",
        "@boost//:preprocessor",
        "@boost//:program_options",
        "@boost//:regex",
        "@boost//:thread",
        "@boost//:variant",
        "@fmt",
        "@double-conversion",
        "@glog",
        #"@libevent",
        #"@libdwarf",
        #"@libiberty",
        #"@libunwind",
        "@zlib",
        "@openssl//:crypto",
        "@openssl//:ssl",

        # "@googletest//:gtest",
        # "@liburing",
        # "@snappy",
        # "@libsodium",
        # "@libaio",
        # "@xz",
    ],
)
