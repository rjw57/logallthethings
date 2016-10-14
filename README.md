# Android sensor and video logger

This is a *very* simple Android sensor and video logger.

Based on the [Android Camera2Video Sample](https://github.com/googlesamples/android-Camera2Video).

## Notes

The CSV format logs two timestamps: the milliseconds since 1st Jan 1920 of the
record being written to the file and a per-sensor timestamp in nanoseconds. The
per-sensor timestamp is only useful for comparing measurements of the same
sensor. If you need to align timestamps, you should note the time at which the
first measurement is taken.

There are some special sensors:

* The ``video`` sensor records two events: ``capture_requested`` when the user
    hits the record button and ``capture_active`` when Android reports that
    video is being recorded.
* The ``location`` sensor records several values at the same sensor timestamp.
    Use the ``has_...`` records to determine which are useful.

## License

Copyright 2016 The Android Open Source Project, Inc.
Copyright 2016 Rich Wareham <rich.logallthethings@richwareham.com>

Licensed to the Apache Software Foundation (ASF) under one or more contributor
license agreements.  See the NOTICE file distributed with this work for
additional information regarding copyright ownership.  The ASF licenses this
file to you under the Apache License, Version 2.0 (the "License"); you may not
use this file except in compliance with the License.  You may obtain a copy of
the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  See the
License for the specific language governing permissions and limitations under
the License.
