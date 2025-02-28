---
UID: NC:extsfns.EXT_ANALYSIS_PLUGIN
title: EXT_ANALYSIS_PLUGIN (extsfns.h)
description: When you write an Analysis Extension, you must implement and export an EXT_ANALYSIS_PLUGIN (_EFN_Analyze) function.
old-location: debugger\_efn_analyze.htm
tech.root: debugger
ms.date: 05/03/2018
keywords: ["EXT_ANALYSIS_PLUGIN callback function"]
ms.keywords: EXT_ANALYSIS_PLUGIN, EXT_ANALYSIS_PLUGIN callback, _EFN_Analyze, _EFN_Analyze callback function [Windows Debugging], debugger._efn_analyze, extsfns/_EFN_Analyze
req.header: extsfns.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - EXT_ANALYSIS_PLUGIN
 - extsfns/EXT_ANALYSIS_PLUGIN
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - extsfns.h
api_name:
 - EXT_ANALYSIS_PLUGIN
---

# EXT_ANALYSIS_PLUGIN callback function


## -description

When you write an <a href="/windows-hardware/drivers/debugger/writing-an-analysis-extension-to-extend--analyze">Analysis Extension</a>, you must implement and export an <b>EXT_ANALYSIS_PLUGIN</b> (<b>_EFN_Analyze</b>) function. When the <a href="/windows-hardware/drivers/debugger/-analyze">!analyze</a> debugger command runs, it calls your <b>_EFN_Analyze</b> so that you can participate in the analysis of a bug check or exception.

## -parameters

### -param Client [in]


A pointer to an <a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugclient4">IDebugClient4</a> interface.

### -param CallPhase [in]


A value in the <a href="/windows-hardware/drivers/ddi/extsfns/ne-extsfns-_fa_extension_plugin_phase">FA_EXTENSION_PLUGIN_PHASE</a> enumeration that specifies which phase of the analysis is currently in progress. Analysis phases include initialization, stack analysis, prebucketing, and post bucketing.

### -param pAnalysis [in]


A pointer to a <b>IDebugFailureAnalysis2</b> interface.

## -returns

If the function succeeds, return <b>S_OK</b>.

## -see-also

<a href="/windows-hardware/drivers/debugger/writing-custom-analysis-debugger-extensions">Writing Custom Analysis Debugger Extension</a>



<a href="/windows-hardware/drivers/debugger/writing-an-analysis-extension-to-extend--analyze">Writing an Analysis Extension Plug-in to Extend !analyze</a>

