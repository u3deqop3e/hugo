// Copyright 2019 The Hugo Authors. All rights reserved.
//
// Licensed under the Apache License, Version 2.0 (the "License");
// you may not use this file except in compliance with the License.
// You may obtain obtain a copy of the License at
// http://www.apache.org/licenses/LICENSE-2.0
//
// Unless required by applicable law or agreed to in writing, software
// distributed under the License is distributed on an "AS IS" BASIS,
// WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
// See the License for the specific language governing permissions and
// limitations under the License.

package deploy

import (
	"fmt"
)

// Target describes a target deployment configuration.
type Target struct {
	Name string
	URL  string

	CloudFrontDistributionID string

	// Optional match patterns for files to include or exclude.
	Include string
	Exclude string
}

// String returns a formatted representation of the deployment target.
func (t Target) String() string {
	if t.Name == "" {
		return t.URL
	}
	return fmt.Sprintf("%s (%s)", t.Name, t.URL)
}