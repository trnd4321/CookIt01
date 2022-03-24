---
name: Release
about: Create Release Procedure checklist
title: '[RELEASE]'
labels: _release_
assignees: ''

---

### ---------------- USE INSTRUCTIONS! ------------------ ###
This is a template issue for release. **DO NOT USE AS IS** please remove non-relevant text (including the instruction).
1. Order of execution should be in the order of the checkboxes
2. Generic procedure is related to all releases while specific package procedures are related only to the relevant packages - please remove irrelevant package procedures.
3. If needed, add any descriptive text before the procedure checkbox list
### ---------------- END OF USE INSTRUCTION ------------- ### 

### Release Content
Please add release content here and link relevant issues.

### Generic Procedure ###
- [ ] Create a version branch - name should be `v_Embedded<ProjectName>_<VersionMajor.Minor>.x`
- [ ] Update release number
- [ ] Update release notes
- [ ] Check NB API for changes from previous release (compare with previous version branch)
- [ ] Build and Test release in CI Embedded_Manual->Embedded_Release configuration

**ONLY IF BUILD/TESTS PASS**
- [ ] Check package on relevant board
- [ ] **IF RELEASE INCLUDES DSP SDK** Run DSP SDK compilation flow and test on relevant board
- [ ] Run Vayyar release script
- [ ] Tag version branch
- [ ] Update release table in https://vayyar.sharepoint.com/sites/IL-DEP-Software/SWWiki/Embedded%20Release%20Procedure.aspx
- [ ] Send mail using release script template to all relevant stakeholders
- [ ] Merge version branch to main branch (master)

### Package Specific ###

**Absinthe**
- [ ] Run DSP SDK compilation flow and test on relevant board (Yes, this is a double check :) ). 
- [ ] Important- Dsp Sdk - We are currently compiling DSP with RI-2020.4-linux. Please be aware of the customer version.
- [ ] Run corner reflector test on the newly created VFS from DSP SDK flow

**TCNA**
- [ ] Run DSP SDK compilation flow and test on relevant board (Yes, this is a double check :) )
- [ ] Important- Dsp Sdk - We are currently compile DSP with RI-2020.4-linux. Please be aware of the customer version.
- [ ] Run corner reflector test on the newly created VFS from DSP SDK flow
