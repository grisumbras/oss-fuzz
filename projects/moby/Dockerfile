# Copyright 2022 Google LLC
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#
################################################################################

FROM gcr.io/oss-fuzz-base/base-builder-go
RUN git clone --depth 1 https://github.com/moby/moby
WORKDIR moby
COPY build.sh etchosts_fuzzer.go oci_fuzzer.go jsonlogbytes_fuzzer.go archive_fuzzers.go tailfile_fuzzer.go jsonfilelog_fuzzer.go mounts_fuzzer.go $SRC/

COPY *.options $SRC/
